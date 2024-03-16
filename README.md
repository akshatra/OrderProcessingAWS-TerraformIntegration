# API-Gateway-SQS-Lambda
 
## The application demonstrates how AWS lambda, SQS, IAM, API Gateway, Cloudwatch services can be leveraged in terraform.

### Project Overview
This project demonstrates how AWS services can seamlessly integrate using infrastructure as code with Terraform. The objective is to establish a functional system on AWS for processing orders, which includes deploying two Lambda functions, an SQS queue, and an API Gateway for receiving requests.

### Key Features
- Utilizes AWS Lambda, SQS, IAM, and API Gateway services within Terraform for infrastructure setup.
- Configures two Lambda functions: one for receiving orders and another for processing orders, interconnected via an SQS queue trigger.
- Employs API Gateway to forward messages to the AddOrder-Lambda for order reception, which subsequently transfers the message to an SQS queue.
- The ProcessOrder-Lambda handles message consumption from the queue and logs an associated message ID on CloudWatch logs.

### Interacting with the API Gateway Service
**Step 1:** Execute `terraform apply` to create the infrastructure.
**Step 2:** Copy the API Gateway URL displayed in the terminal and paste it into the `endpoint` variable within `src/REST-Interface.py`.
**Step 3:** Run the `REST-Interface.py` script to activate the API Gateway.
