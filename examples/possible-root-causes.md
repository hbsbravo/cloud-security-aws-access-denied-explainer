\# Possible Root Causes for AWS Access Denied Events



\## IAM Policy Deny



The identity does not have an allow statement for the requested action, or an explicit deny blocks the action.



\## Resource Policy Deny



The resource policy, such as an S3 bucket policy or Secrets Manager resource policy, denies access.



\## Service Control Policy Restriction



An AWS Organizations SCP prevents the account or principal from performing the action.



\## KMS Key Policy Restriction



The user may have access to the S3 object or secret but not permission to use the required KMS key.



\## Missing Trust Relationship



The user or role may not be allowed to assume the role needed for the action.



\## Region or Account Mismatch



The request may be targeting the wrong AWS region or account.

