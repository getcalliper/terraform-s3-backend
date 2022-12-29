# terraform-s3-backend

Forked and simplified from [this config](https://github.com/DNXLabs/terraform-aws-backend).

**To deploy this you should be using credentials for the Calliper Config AWS account.**

Contains the S3 Bucket, DynamoDB and permissions for supporting Terraform Backend with S3 in a multi-account architecture where:

- Terraform State lives in the Config AWS account.
- Dev and Prod users access it by assuming the `terraform-backend` role defined here.

[Terraform S3 Backend docs](https://www.terraform.io/docs/backends/types/s3.html)
