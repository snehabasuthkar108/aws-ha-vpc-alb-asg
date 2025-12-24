# Highly Available AWS VPC with ALB and Auto Scaling

## Overview
This project demonstrates a production-style AWS infrastructure built using a secure VPC design. The architecture uses public and private subnets across multiple Availability Zones, with application servers running in private subnets and exposed via an Application Load Balancer.

## Architecture
![Architecture](architecture/aws-ha-vpc-architecture.png)

## Key Components
- Custom VPC (10.0.0.0/16)
- Public and Private Subnets (Multi-AZ)
- Internet Gateway and NAT Gateway
- Bastion Host for secure SSH access
- Launch Template and Auto Scaling Group
- Application Load Balancer
- Target Groups with health checks

## Traffic Flow
- User → Application Load Balancer → EC2 instances (private subnets)
- Admin → Bastion Host → Private EC2 instances

## Security Highlights
- No public IPs on application servers
- SSH access only via Bastion Host
- Security Groups follow least privilege
- Private subnet instances access internet via NAT Gateway

## Result
The application is successfully deployed in private subnets and is accessible via the ALB DNS name. The setup demonstrates high availability, scalability, and secure network design.

## Learning Outcome
- VPC and subnet design
- Load balancing and auto scaling
- Secure access using Bastion Host
- Debugging real-world ALB 503 issues

