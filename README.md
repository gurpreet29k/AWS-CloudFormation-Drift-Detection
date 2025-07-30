# AWS CloudFormation Drift Detection & Lambda Automation Project

This project demonstrates how to:
1. Create and manage AWS resources using **CloudFormation**.
2. Detect **manual changes (drift)** in a CloudFormation stack.
3. Automate tasks using **AWS Lambda** triggered by **Amazon EventBridge** (scheduled every 2 minutes).

---

## 🚀 Features
- **CloudFormation Stack (YAML):**
  - Deploys an **EC2 instance, VPC, Subnet, Security Groups, IAM role**.
  - Provides an Infrastructure-as-Code (IaC) foundation for reproducible AWS environments.

- **Drift Detection:**
  - After manual changes to the EC2 instance, drift detection is used to identify differences between the deployed resources and the CloudFormation template.

- **Lambda Function (Python):**
  - Automates a simple task (describe task purpose briefly, e.g., rolleback changes in security group, rollback IAM role change, etc.).
  - Integrated with **EventBridge** to run automatically every 2 minutes.

---

## 🛠 Tech Stack
- **AWS CloudFormation** (YAML)
- **AWS Lambda** (Python 3.x)
- **Amazon EventBridge**
- **AWS EC2**
- **IAM (for permissions)**

<img width="1047" height="736" alt="image" src="https://github.com/user-attachments/assets/2e4aa441-b555-495c-9e7e-2aed8d55c9e9" />

---


---

## ⚙️ Setup Instructions

### 1️⃣ Deploy the CloudFormation Stack:
1. Navigate to the AWS Management Console → CloudFormation.
2. Create a new stack using the `cloudformation - Stack.yaml`.
3. Wait for stack creation to complete and verify EC2 instance deployment.

### 2️⃣ Test Drift Detection:
1. Make a manual change to the EC2 instance (e.g., add a new inbound rule to the attached security group).
2. In the CloudFormation console, select **Actions → Detect Drift**.
3. Review drift results to analyze differences between actual and template-defined resources.

### 3️⃣ Configure Lambda & EventBridge:
1. Create a Lambda function and upload `lambda_function.py` code.
2. Attach necessary IAM roles for Lambda execution.
3. Create an EventBridge rule with a schedule expression:
   rate(2 minutes)
5. Set the Lambda function as the target for the EventBridge rule.

---

## 📊 Use Cases
- Understanding **Infrastructure-as-Code (IaC)** workflows with AWS CloudFormation.
- Practicing **drift detection** to maintain compliance between deployed and defined infrastructure.
- Automating recurring tasks with **Lambda + EventBridge** scheduling.

---

## 🔑 Prerequisites
- AWS account with admin or necessary IAM permissions.
- AWS CLI configured (optional but recommended).
- Basic knowledge of Python and YAML.

---

## 📜 License
This project is for **educational purposes** and showcases AWS IaC and automation concepts.

---

## ✍️ Author
**Gurpreet Kaur**  



