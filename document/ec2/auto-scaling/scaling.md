If the Auto Scaling group (ASG) is using EC2 as the health check type and the Application Load Balancer (ALB) is using its in-built health check, there may be a situation where 
* The ALB health check fails because the health check pings fail to receive a response from the instance.
* At the same time, ASG health check can come back as successful because it is based on EC2 based health check.

Therefore, in this scenario, the ALB will remove the instance from its inventory, however, the Auto Scaling Group will fail to provide the replacement instance.