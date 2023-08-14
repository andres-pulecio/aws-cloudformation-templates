# AWS CloudFormation Template - VPC and Resources

This CloudFormation template sets up a Virtual Private Cloud (VPC) with various resources, including EC2 instances, DynamoDB tables, Lambda functions, and an API Gateway for a multiple-choice question application.

## Usage

1. Make sure you have the AWS Command Line Interface (CLI) installed and configured.
2. Deploy the CloudFormation stack using the AWS CLI or AWS Management Console.

### Parameters

- `KeyName`: The key pair used to launch EC2 instances.
- `LatestAmiId`: The latest Amazon Linux AMI ID.
- `LabUserId`: Session user ARN.
- `QuestionTableRead`: Read capacity units for DynamoDB table.
- `QuestionTableWrite`: Write capacity units for DynamoDB table.

### Resources

The template creates the following resources:

- A VPC with an Internet Gateway.
- Public and Private Subnets.
- IAM Roles and Policies.
- A Lambda function to create a VPC in another region.
- DynamoDB tables for storing answers.
- An API Gateway to collect student answers.
- An S3 bucket for hosting HTML files.

## Credits

This template is created using AWS CloudFormation and includes resources for various AWS services.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
