\# Infrastructure



This folder contains infrastructure-as-code artifacts for the AWS Access Denied Explainer cloud security project.



\## Included Files



\- `cloudformation-template.yaml` — Starter AWS CloudFormation template for the Access Denied detection and alerting architecture.



\## Resources Defined



The CloudFormation template provisions the following resources:



\- S3 bucket for log storage

\- DynamoDB table for Access Denied event metadata

\- SNS topic and email subscription for alerts

\- Lambda function for Access Denied event processing

\- EventBridge rule for detecting Access Denied events

\- IAM role for Lambda execution

\- CloudWatch log group for Lambda logs



\## Architecture Purpose



The infrastructure supports a detection workflow where AWS authorization failures are captured, processed, stored, and reported.



Basic event flow:



```text

AWS API Call

&#x20;  ↓

CloudTrail Event

&#x20;  ↓

EventBridge Rule

&#x20;  ↓

Lambda Processor

&#x20;  ↓

SNS Alert + DynamoDB Metadata + CloudWatch Logs

