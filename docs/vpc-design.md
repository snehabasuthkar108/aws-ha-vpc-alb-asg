# VPC Design

## Overview
A custom VPC was created using CIDR block 10.0.0.0/16. The VPC spans two Availability Zones (us-east-1a and us-east-1b) to ensure high availability.

## Subnet Layout
- Two public subnets for:
  - Application Load Balancer
  - Bastion Host
- Two private subnets for:
  - Application EC2 instances managed by Auto Scaling Group

## Networking Components
- Internet Gateway attached to the VPC
- NAT Gateway in public subnet to allow outbound internet access for private instances

## Screenshot
![VPC Design](../screenshots/vpc-design.png)
