\# Security Scenarios



\## Scenario 1: S3 Access Denied Alerts with KMS



This scenario focuses on detecting unauthorized S3 access attempts when S3 objects are protected by AWS KMS.



\### Security Goal



Detect when a user attempts to access an S3 object but is denied because of IAM, bucket policy, or KMS key policy restrictions.



\### AWS Services Used



\- Amazon S3

\- AWS KMS

\- AWS CloudTrail

\- Amazon CloudWatch

\- Amazon SNS



\### Detection Logic



CloudTrail records denied S3 API activity. CloudWatch and/or EventBridge detect Access Denied patterns. SNS sends alerts containing the denied action, user identity, and affected resource.



\## Scenario 2: DynamoDB and Secrets Manager Access Denied Events



This scenario focuses on detecting denied operations against DynamoDB and AWS Secrets Manager.



\### Security Goal



Detect unauthorized attempts to perform restricted actions such as creating DynamoDB tables or creating Secrets Manager secrets.



\### AWS Services Used



\- Amazon DynamoDB

\- AWS Secrets Manager

\- AWS CloudTrail

\- Amazon EventBridge

\- AWS Lambda

\- Amazon SNS



\### Detection Logic



CloudTrail records the denied API call. EventBridge routes the event to Lambda. Lambda extracts details such as user identity, operation, resource, and error message. SNS sends a real-time alert.

