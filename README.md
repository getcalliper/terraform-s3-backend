# terraform-s3-backend

Forked and simplified from [this config](https://github.com/DNXLabs/terraform-aws-backend).

**To deploy this you should be using credentials for the Calliper Config AWS account.**

Contains the infra to support Terraform Backend for our [Dev and Prod AWS environments](https://github.com/getcalliper/calliper-infra/blob/main/terraform/remote_backend.tf) with S3 in a multi-account architecture where:

- Terraform State for Dev and Prod lives in the Config AWS account.
- Dev and Prod users access it by assuming the `terraform-backend` role defined here.

Note that this config carries its own state file which is committed to git. 
It does not use remote backend itself!

[Terraform S3 Backend docs](https://www.terraform.io/docs/backends/types/s3.html)
