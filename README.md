# Highly Available AWS VPC with ALB and Auto Scaling

## Overview
This project demonstrates a production-style AWS infrastructure using a secure VPC with public and private subnets across multiple Availability Zones. Application servers run in private subnets and are accessed securely via a Bastion Host and exposed using an Application Load Balancer.

## Architecture
![Architecture](architecture/aws-ha-vpc-architecture.png)

## Key Components
- Custom VPC (Multi-AZ)
- Public & Private Subnets
- Internet Gateway & NAT Gateway
- Bastion Host
- Auto Scaling Group
- Application Load Balancer

## Status
🚧 In progress
