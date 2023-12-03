**Question**

A startup wants to create a highly available architecture for its multi-tier application. Currently, the startup manages a single Amazon EC2 instance along with a single Amazon RDS MySQL DB instance. The startup has hired you as an AWS Certified Solutions Architect - Associate to build a solution that meets these requirements while minimizing the underlying infrastructure maintenance effort.
What will you recommend?

**A. Create an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances across two Availability Zones. Configure an Application Load Balancer having a target group of these Amazon EC2 instances. Set up Amazon RDS MySQL DB in a multi-AZ configuration**

B. Create an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances across two Availability Zones. Configure an Application Load Balancer having a target group of these Amazon EC2 instances. Set up a read replica of the Amazon RDS MySQL DB in another Availability Zone

C. Create an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances in a single Availability Zone. Configure an Application Load Balancer having a target group of these Amazon EC2 instances. Set up Amazon RDS MySQL DB in a multi-AZ configuration

D. Provision a second Amazon EC2 instance in another Availability Zone. Provision a second Amazon RDS MySQL DB in another Availabililty Zone. Leverage Amazon Route 53 for equal distribution of incoming traffic to the Amazon EC2 instances. Use a custom script to sync data across the two MySQL DBs

**Explained**

In a multi-AZ deployment, Amazon RDS automatically provisions and maintains a synchronous “standby” replica in a different Availability Zone. Updates to your DB Instance are synchronously replicated across Availability Zones to the standby to keep both in sync and protect your latest database updates against DB instance failure.


=====================================================>

**Question**

A company has a two-tier environment in its on-premises data center which is composed of an application tier and database tier. You are instructed to migrate their environment to the AWS cloud, and to design the subnets in their VPC with the following requirements:

1. There is an application load balancer that would distribute the incoming traffic among the servers in the application tier.
2. The application tier and the database tier must not be accessible from the public Internet. The application tier should only accept traffic coming from the load balancer.
3. The database tier contains very sensitive data. It must not share the same subnet with other AWS resources and its custom route table with other instances in the environment.
4. The environment must be highly available and scalable to handle a surge of incoming traffic over the Internet.

How many subnets should you create to meet the above requirements?

A. 2

B. 3

C. 4

D. 6

**Explained**

To summarize, we need to have one private subnet for the application tier and another one for the database tier. We then need to create another public subnet in the same Availability Zone where the private EC2 instances are hosted in order to properly connect the public Internet-facing load balancer to your instances. This means that we have to use a total of 3 subnets consisting of 2 private subnets and 1 public subnet.

To meet the requirement of high availability, we have to deploy the stack to two Availability Zones. This means that you have to double the number of subnets you are using. Take note as well that you must create the corresponding public subnet in the same Availability Zone of your private EC2 servers in order for it to properly communicate with the load balancer.