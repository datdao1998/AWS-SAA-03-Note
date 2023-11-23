**Question**

You have deployed a database technology that has a synchronous replication mode to survive disasters in data centers. The database is therefore deployed on two Amazon EC2 instances in two Availability Zones (AZs). The database must be publicly available so you have deployed the Amazon EC2 instances in public subnets. The replication protocol currently uses the Amazon EC2 public IP addresses.
What can you do to decrease the replication cost?

A. Assign elastic IP address (EIP) to the Amazon EC2 instances and use them for the replication

B. Use an Elastic Fabric Adapter (EFA)

**C. Use the Amazon EC2 instances private IP for the replication**

D. Create a Private Link between the two Amazon EC2 instances

**Explained**

The source of the cost is that traffic between two EC2 instances is going over the public internet, thus incurring high costs. Here, the correct answer is to use Private IP, so that the network remains private, for a minimal cost.

=====================================================>

**Question**
A systems administration team has a requirement to run certain custom scripts only once during the launch of the Amazon Elastic Compute Cloud (Amazon EC2) instances that host their application.
Which of the following represents the best way of configuring a solution for this requirement with minimal effort?

**A. Run the custom scripts as user data scripts on the Amazon EC2 instances**

B. Update Amazon EC2 instance configuration to ensure that the custom scripts, added as user data scripts, are run only during the boot process 

C. Run the custom scripts as instance metadata scripts on the Amazon EC2 instances

D. Use AWS CLI to run the user data scripts only once while launching the instance

**Explained**

When you launch an instance in Amazon EC2, you have the option of passing user data to the instance that can be used to perform common automated configuration tasks and even run scripts after the instance starts. You can pass two types of user data to Amazon EC2: shell scripts and cloud-init directives.

By default, user data scripts and cloud-init directives run only during the boot cycle when you first launch an instance. Hence, no extra configuration is needed, apart from including the custom scripts in user data scripts.

=====================================================>

**Question**

The DevOps team at an e-commerce company has deployed a fleet of Amazon EC2 instances under an Auto Scaling group (ASG). The instances under the ASG span two Availability Zones (AZ) within the us-east-1 region. All the incoming requests are handled by an Application Load Balancer (ALB) that routes the requests to the Amazon EC2 instances under the Auto Scaling Group. As part of a test run, two instances (instance 1 and 2, belonging to AZ A) were manually terminated by the DevOps team causing the Availability Zones (AZ) to have unbalanced resources. Later that day, another instance (belonging to AZ B) was detected as unhealthy by the Application Load Balancer's health check.
Can you identify the correct outcomes for these events? (Select two)

**A. As the resources are unbalanced in the Availability Zones, Amazon EC2 Auto Scaling will compensate by rebalancing the Availability Zones. When rebalancing, Amazon EC2 Auto Scaling launches new instances before terminating the old ones, so that rebalancing does not compromise the performance or availability of your application**

**B. Amazon EC2 Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it. Later, another scaling activity launches a new instance to replace the terminated instance**

C. Amazon EC2 Auto Scaling creates a new scaling activity for launching a new instance to replace the unhealthy instance. Later, Amazon EC2 Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it

D. As the resources are unbalanced in the Availability Zones, Amazon EC2 Auto Scaling will compensate by rebalancing the Availability Zones. When rebalancing, Amazon EC2 Auto Scaling terminates old instances before launching new instances, so that rebalancing does not cause extra instances to be launched

E. Amazon EC2 Auto Scaling creates a new scaling activity to terminate the unhealthy instance and launch the new instance simultaneously

**Explained**

Amazon EC2 Auto Scaling helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application. You create collections of EC2 instances, called Auto Scaling groups. You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes below this size. Actions such as changing the Availability Zones (AZ) for your group or explicitly terminating or detaching instances can lead to the Auto Scaling group becoming unbalanced between Availability Zones. Amazon EC2 Auto Scaling compensates by rebalancing the Availability Zones.

When rebalancing, Amazon EC2 Auto Scaling launches new instances before terminating the old ones, so that rebalancing does not compromise the performance or availability of your application. Therefore, this option is correct.

However, the scaling activity of Auto Scaling works in a different sequence compared to the rebalancing activity. Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it. Later, another scaling activity launches a new instance to replace the terminated instance.

=====================================================>

**Question**

You are deploying a critical monolith application that must be deployed on a single web server, as it hasn't been created to work in distributed mode. Still, you want to make sure your setup can automatically recover from the failure of an Availability Zone (AZ).
Which of the following options should be combined to form the MOST cost-efficient solution? (Select three)

**A. Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=1, desired=1**

**B. Create an elastic IP address (EIP) and use the Amazon EC2 user-data script to attach it**

**C. Assign an Amazon EC2 Instance Role to perform the necessary API calls**

D. Create a Spot Fleet request 

E. Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=2, desired=2

F. Create an Application Load Balancer and a target group with the instance(s) of the Auto Scaling Group

**Explained**

Note 1:

Application Load Balancer (ALB) operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses, and Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
An Elastic IP address is a static IPv4 address designed for dynamic cloud computing. An Elastic IP address is associated with your AWS account. With an Elastic IP address, you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account.
Now, between the ALB and the Elastic IP. If we use an ALB, things will still work, but we will have to pay for the provisioned ALB which sends traffic to only one Amazon EC2 instance. Instead, to minimize costs, we must use an Elastic IP.

Note 2:

For that Elastic IP to be attached to our Amazon EC2 instance, we must use an EC2 user data script, and our Amazon EC2 instance must have the correct IAM permissions to perform the API call, so we need an Amazon EC2 instance role.