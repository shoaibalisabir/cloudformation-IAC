# Highly Available Microservices VPC

This project is an AWS CloudFormation template designed to create a highly available microservices architecture using AWS resources. It includes both public and private subnets, an Application Load Balancer (ALB), and an Auto Scaling Group (ASG) for dynamic scaling.

## Overview

This CloudFormation template sets up the following resources:

- A Virtual Private Cloud (VPC) with CIDR block `10.0.0.0/16`.
- Two public subnets and two private subnets to host services.
- An Internet Gateway for public access.
- A NAT Gateway for private subnet outbound traffic.
- An Application Load Balancer to distribute incoming traffic.
- An Auto Scaling Group to manage EC2 instances based on demand.
- Security Groups to control access to the resources.

## Features

- **Highly Available Architecture**: Utilizes multiple availability zones for redundancy.
- **Auto Scaling**: Automatically adjusts the number of EC2 instances based on traffic demand.
- **Load Balancing**: Distributes incoming traffic across multiple instances for better performance.
- **Private Subnets**: Ensures that backend services are not directly accessible from the internet.

## Static HTML Website

In addition to the CloudFormation template for deploying microservices, this project includes a single static HTML website. This static website serves as a simple front-end interface for users to interact with the microservices once they are deployed.

### Features of the Static HTML Website

- **Basic Interface**: Provides a straightforward user interface demonstrating how users might interact with the microservices.
- **Deployment Example**: While the website does not showcase dynamic functionality, it illustrates how a static front-end can be hosted alongside microservices.

## Prerequisites

- AWS Account
- AWS CLI installed and configured
- Basic understanding of AWS services and CloudFormation

## Customization

You can modify the following parameters in the YAML file:

- **InstanceType**: Change the instance type in the `LaunchTemplate` section based on your needs.
- **ImageId**: Update the AMI ID for the EC2 instances to the latest version.
- **Scaling Policies**: Adjust the scaling parameters to fit your application's demand.

## Cleanup

To delete the resources created by this stack, run:

```bash
aws cloudformation delete-stack --stack-name MicroservicesStack
```

## Acknowledgments

- [AWS CloudFormation Documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)
- [AWS EC2 Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html)

