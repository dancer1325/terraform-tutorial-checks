# Learn Terraform - Checks
* This is a companion repository for HashiCorp's [Validate Infrastructure Using Checks](https://developer.hashicorp.com/terraform/tutorials/configuration-language-checks)

## Goals 
* Checks
  * how to configure
  * how to use  

## Prerequisites
* Terraform [v1.2+](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli) installed locally
* AWS account with [associated credentials](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#authentication-and-configuration)
  * via
    * add in the 'provider' block
    * environment variables
      * 'AWS_ACCESS_KEY_ID'
      * 'AWS_SECRET_ACCESS_KEY'
      * 'AWS_REGION'
    * credential files
      * `aws config` & pass the 'AWS_ACCESS_KEY_ID' & 'AWS_SECRET_ACCESS_KEY'

## How to run?
* `terraform init`
* `terraform plan`
  * Check how the checks run, but both require to apply
  * Problems:
    * Problem1: NO output
      * Solution: Update aws.versions
    * Problem2: "data "aws_ami" filter Error: Your query returned no results."
      * Solution: filter by another value
* `terraform apply`
  * Check how the check also run
  * Problems:
    * Problem1: Open in your desired browser 'output lb_endpoint', and get 502
      * Solution: TODO:

## Notes
* [aws_acm_certificate](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/acm_certificate)