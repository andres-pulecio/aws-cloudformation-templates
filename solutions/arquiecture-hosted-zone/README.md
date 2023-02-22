# Arquitecture Hosted Zone
These templates create an infrastructure that describes an example, simple web application running in the AWS cloud as follows:

* One Amazon Virtual Private Cloud  (Amazon VPC), with 2 public and 2 private subnets across 2 availability zones  of a given region, such as the us-east-1 region.
* One Auto Scaling group  with a minimum of 2 Amazon Elastic Compute Cloud  (Amazon EC2) instances, and a maximum of 4. You'll launch such instances in the 2 private subnets, and you'll use such instances to run a simple web application.
* One Application Load Balancer  with an Internet-facing endpoint; this load balancer will be fronting your EC2 instances.
* One Amazon Route 53  hosted zone , where you'll store an alias  record that points to your load balancer.
## Infrastructure

![arquitecture-zone](https://user-images.githubusercontent.com/53886913/220493903-c3482980-a952-4e9b-9129-063632e1c29c.png)

## Descriptions Stacks

* One template for VPC-related resources.
* One template for hosted zone.
* One template for application and load balancer security groups.
* One template for application stack, including load balancer, EC2 instances, and a DNS record to add to the hosted zone created with a previous template.

## Steps 

1. Creating the VPC stackHeader 
2. Creating  Cloud9 environment
3. Creating the hosted zoneHeader 
4. Creating security groupsHeader 
5. Creating the application stackHeader 
