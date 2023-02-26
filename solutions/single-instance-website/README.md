# Single Instance Website
This template create:
* The root stack (which is also a parent stack for the first level stacks). This root stack will contain all the other stacks.
* The VPC stack. This contains a simple VPC template which the EC2 instance will be placed into.
* The IAM instance role stack. This contains the IAM instance role template decoupled form your EC2 template.
* The EC2 stack. This contains the EC2 instance you have defined in your previous CloudFormation template.

## Prerequisites
Whilst single templates can be deployed from your local machine, Nested Stacks require that the nested templates are stored in an S3 bucket.

You have created simple CloudFormation template which created S3 bucket. Please make a note of the bucket name.

For example:

Bucket name: cfn-workshop-s3-s3bucket-2cozhsniu50t

If you don't have S3 bucket, please go back to [S3simple.yaml](../../S3/S3simple.yaml) create one.

*Top level and first level hierarchy of nested stacks.*

![top-level](https://user-images.githubusercontent.com/53886913/219972549-17ba8b71-3e53-4282-bd7d-c0af7f8732e2.png)

*The following diagram represents high level overview of the infrastructure:*

![lab1-architecture](https://user-images.githubusercontent.com/53886913/220818740-7b1037be-9233-46e3-b818-5495e515bfe3.jpg)

