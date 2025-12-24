# Security Design

## Security Groups
- ALB: HTTP 80 from internet
- Bastion: SSH 22 from my IP
- App EC2: Port 8000 from ALB SG, SSH from Bastion SG

## Network ACLs
- Default NACLs used (stateless)

![SSH](../screenshots/scp-ssh.png)

