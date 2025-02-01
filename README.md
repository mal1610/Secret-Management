# Secret-Management

1. What is needed to authorize your EC2 to retrieve secrets from the AWS Secrets Manager?

- We need to create and attach an IAM role that grants the EC2 instance permission through the IAM policy.

2. Derive the IAM policy (i.e. JSON) Using the secret name prod/cart-service/credentials, derive a sensible ARN as the specific resource for access
```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "secretsmanager:GetSecretValue",
      "Resource": "arn:aws:secretsmanager:ap-southeast-1:1111222233334444:secret:prod/cart-servce/credentials*"
    }
  ]
}

```
