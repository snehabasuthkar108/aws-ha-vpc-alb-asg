# Auto Scaling Group and Load Balancer

## Launch Template
The launch template defines:
- Ubuntu AMI
- t3.micro instance type
- Application security group
- User data to start Python HTTP server on port 8000

## Auto Scaling Group
- Desired capacity: 2
- Min: 1, Max: 4
- Instances launched in private subnets across two AZs
- Target Group attached for automatic registration

## Application Load Balancer
- Internet-facing ALB
- Listener: HTTP : 80
- Forwards traffic to Target Group on port 8000

## Screenshots
![ASG Running](../screenshots/asg-running.png)  
![Target Group Healthy](../screenshots/target-group-healthy.png)  
![ALB Active](../screenshots/alb-active.png)
