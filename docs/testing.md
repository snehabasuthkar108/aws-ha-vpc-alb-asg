# Testing & Validation

## SSH via Bastion Host
The bastion host was used as the only entry point to access private EC2 instances.

- SSH key copied securely using SCP
- SSH access to private instances was successful only via bastion host

![SSH via Bastion](../screenshots/scp-ssh.png)

---

## Application Output via ALB
The application was accessed using the Application Load Balancer DNS name.

Each EC2 instance serves a unique response identifying itself and its Availability Zone.

### Server 1 Response (us-east-1a)
![Server1](../screenshots/serveroutput1.png)

### Server 2 Response (us-east-1b)
![Server2](../screenshots/serveroutput2.png)

---

## Result and Validation

### Expected Behavior
- Application should be reachable only through the ALB
- EC2 instances should remain in private subnets
- Traffic should be distributed across multiple Availability Zones

### Observed Behavior
- ALB DNS successfully served the application
- On refreshing the browser multiple times:
  - Requests alternated between Server 1 and Server 2
  - Each response confirmed a different Availability Zone
- All targets were marked **Healthy** in the target group

### Validation Outcome
✅ ALB correctly distributes traffic using round-robin  
✅ High availability achieved across multiple AZs  
✅ Private EC2 instances are not directly exposed to the internet  
✅ Bastion host access model works as expected  

**Final Result:**  
Traffic successfully routed: **User → ALB → Private EC2 instances (Auto Scaling Group)**
