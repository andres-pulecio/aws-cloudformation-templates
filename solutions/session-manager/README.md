# Session manager
[Session Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html) is a fully managed AWS Systems Manager capability that lets you manage your Amazon EC2 instances through an interactive one-click browser-based terminal or via the AWS CLI.

Session Manager has several benefits over using SSH:

* No need to manage SSH keys.
* No need to open up any inbound ports in Security Groups.
* You can use IAM policies and users to control access to your instances.
* Commands and responses can be logged to Amazon CloudWatch and to an S3 bucket.

![ssm-sm-1](https://user-images.githubusercontent.com/53886913/216796075-97642d06-21b8-4adf-acf9-c388ca4bc3d7.png)
