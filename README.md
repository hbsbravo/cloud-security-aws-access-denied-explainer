# Cloud Security AWS Access Denied Explainer


## Overview



This project is a cloud security detection and troubleshooting design for AWS Access Denied events. The goal is to help identify why access failures occur across IAM policies, resource policies, Service Control Policies, S3 bucket policies, KMS key policies, and Secrets Manager policies.



## Security Focus Areas



\- AWS IAM troubleshooting

\- CloudTrail event monitoring

\- EventBridge detection rules

\- Lambda-based event processing

\- SNS alerting

\- DynamoDB event metadata storage

\- CloudWatch monitoring

\- KMS and Secrets Manager access control

\- Cloud security detection engineering



## Architecture


```text


with this:

````markdown
```text
AWS API Call
   ↓
CloudTrail Event
   ↓
EventBridge Rule
   ↓
Lambda Processor
   ↓
SNS Alert + DynamoDB Metadata + CloudWatch Logs

