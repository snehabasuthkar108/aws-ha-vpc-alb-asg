# Security Design

## Security Groups

### Bastion Host SG
- Allows SSH (22) from administrator IP only

### Application EC2 SG
- Allows SSH (22) from Bastion Host SG
- Allows TCP 8000 only from ALB SG

### ALB SG
- Allows HTTP (80) from the internet

## Security Principles
- No public IPs on private EC2 instances
- SSH access strictly via Bastion Host
- Least privilege enforced at network layer
