# terraform-bake-ami-shared-resources

[![Release](https://img.shields.io/github/release/traveloka/terraform-bake-ami-shared-resources.svg)](https://github.com/traveloka/terraform-bake-ami-shared-resources/releases)
[![Last Commit](https://img.shields.io/github/last-commit/traveloka/terraform-bake-ami-shared-resources.svg)](https://github.com/traveloka/terraform-bake-ami-shared-resources/commits/master)
![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)

## Description

A terraform module which provisions shared (accross-services) resources required by https://github.com/traveloka/terraform-aws-bake-ami


## Prerequisites

## Dependencies

This Terraform module have no dependencies to another modules


## Getting Started
<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| aws | n/a |
| random | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| appbin\_deep\_archive\_transition\_days | The number of days before objects in the application binary bucket are moved to the glacier deep archive class | `string` | `"60"` | no |
| appbin\_expiration\_days | The number of days before objects in the application binary bucket are deleted | `string` | `"365"` | no |
| appbin\_standard\_ia\_transition\_days | The number of days before objects in the application binary bucket are moved to the standard IA class | `string` | `"30"` | no |
| appbin\_writers | The IAM ARNs from other AWS Accounts that should be given access to write to the application binary bucket | `list` | n/a | yes |
| base\_ami\_owners | The AWS account IDs that owns the base AMI | `list` | n/a | yes |
| lambda\_function\_arn | The arn of the AMI sharing lambda function | `string` | n/a | yes |
| logging\_bucket | The name of the bucket that will receive the log objects of all S3 resources in this module | `string` | n/a | yes |
| product\_domain | The product domain which the created resources belong to | `string` | n/a | yes |
| subnet\_tier | The tier of the subnet where CodeBuild and AMI baking instances should run, i.e. either 'public' or 'app' | `string` | `"public"` | no |
| vpc\_id | The id of the VPC where CodeBuild and AMI baking instances will reside | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| application\_binary\_bucket | n/a |
| codebuild\_cache\_bucket | n/a |
| codebuild\_role\_arn | n/a |
| codepipeline\_artifact\_bucket | n/a |
| codepipeline\_role\_arn | n/a |
| events\_role\_arn | n/a |
| subnet\_id | n/a |
| template\_instance\_profile\_name | n/a |
| template\_instance\_security\_group | n/a |
| vpc\_id | n/a |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Contributing

This module accepting or open for any contributions from anyone, please see the [CONTRIBUTING.md](https://github.com/traveloka/terraform-aws-private-route53-zone/blob/master/CONTRIBUTING.md) for more detail about how to contribute to this module.

## License

This module is under Apache License 2.0 - see the [LICENSE](https://github.com/traveloka/terraform-aws-private-route53-zone/blob/master/LICENSE) file for details.