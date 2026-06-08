\# Lessons Learned



\## Key Lessons



\- CloudTrail logging is powerful but requires careful configuration.

\- IAM permissions must be precise for each service integration.

\- EventBridge rules need accurate event patterns to avoid missed detections.

\- Lambda functions must be designed to process events efficiently.

\- SNS alerting requires testing to confirm reliable email delivery.

\- Cloud security troubleshooting often requires checking multiple policy layers.



\## Challenges Encountered



\- Configuring CloudTrail to capture useful Access Denied events.

\- Tuning EventBridge rules for specific denial patterns.

\- Processing larger logs in Lambda.

\- Configuring reliable SNS notifications.

\- Attempting API Gateway integration.



\## Future Improvements



\- Add anomaly detection for unusual denial patterns.

\- Expand support to additional AWS services.

\- Integrate with AWS Organizations and SCP analysis.

\- Export events to a SIEM.

\- Build deployable CloudFormation or Terraform templates.

