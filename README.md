# Terraform Test
## Background
This is to test your understanding of infrastructure as a code. Port numbers can be arbitrary, as long as they all line up. We should be able to generate a valid plan using an AWS provider; however the infrastructure does not need to work to the point of being spun up. Feel free to make up any necessary details as need be.
Task & Requirements
Using the AWS Provider, build the following:
- Fleet of application server instances with AWS ELB
- Fleet of worker server instances
- Aurora database cluster (MySQL Engine, at least 3 instances)
- These should be contained in a VPC with the appropriate security groups and subnets.

Bonus:

- Sensible directory and file structure
- Provide for mapping cloud assets via AWS API (tags)
- Cloudfront
- Terraform modules
- "Precompilation" of terraform code files to allow for more advanced topology patterns.
- Other creative solutions/ideas

# use
setup your credentials in ~/.aws

terraform init
terraform plan
don't apply, it is **untested**

## I forked the code from project below:

# terraform-aws-vpc

This repository contains a [Terraform][] project that builds [Scenario 2: VPC
with Public and Private Subnets][scenario_two] from the [AWS documentation][].
It's from [this blog post][blog_post] describing how it all works and is
designed to give a working example which can the basis of something much more
complex.

## Usage

`terraform.tfvars` holds variables which should be overriden with valid ones.

### Plan

```
terraform plan -var-file terraform.tfvars
```

### Apply

```
terraform apply -var-file terraform.tfvars
```

### Destroy

```
terraform destroy -var-file terraform.tfvars
```

## Author

Copyright (c) 2015 Nick Charlton <nick@nickcharlton.net>. MIT Licensed.

[Terraform]: http://terraform.io
[scenario_two]: http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario2.html
[AWS documentation]: http://aws.amazon.com/documentation/
[blog_post]: https://nickcharlton.net/posts/terraform-aws-vpc.html
