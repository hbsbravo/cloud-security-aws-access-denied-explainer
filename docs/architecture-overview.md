# Architecture Overview

The AWS Access Denied Explainer is designed to detect, process, and explain authorization failures in AWS environments.

## Core Services

- AWS CloudTrail logs API activity and Access Denied events.
- Amazon EventBridge routes matching events to processing logic.
- AWS Lambda analyzes the denied event and extracts key details.
- Amazon SNS sends real-time email alerts.
- Amazon CloudWatch provides monitoring and dashboard visibility.
- Amazon S3 stores logs for extended analysis.
- Amazon DynamoDB stores historical metadata about denied events.
- AWS KMS supports encryption enforcement scenarios.
- AWS Secrets Manager supports sensitive-data access control monitoring.

## Event Flow

1. A user or service makes an AWS API request.
2. AWS denies the action because of IAM, SCP, bucket policy, KMS, or resource policy restrictions.
3. CloudTrail records the denied API event.
4. EventBridge matches the Access Denied pattern.
5. Lambda processes the event.
6. SNS sends an alert.
7. CloudWatch and DynamoDB support monitoring and historical analysis.