# Testing and Validation

## SSH Validation
- SSH access tested using Bastion Host
- Private EC2 accessed successfully via Bastion

![SSH Bastion](../screenshots/ssh-bastion.png)

## Application Validation
- Python HTTP server started on both EC2 instances
- Application accessed using ALB DNS name
- Load balancing confirmed by different server responses

![Server 1](../screenshots/app-server-1.png)  
![Server 2](../screenshots/app-server-2.png)
