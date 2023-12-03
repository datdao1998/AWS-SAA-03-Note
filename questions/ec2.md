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


=====================================================>

**Question**

You are automating the creation of EC2 instances in your VPC. Hence, you wrote a python script to trigger the Amazon EC2 API to request 50 EC2 instances in a single Availability Zone. However, you noticed that after 20 successful requests, subsequent requests failed.

What could be a reason for this issue and how would you resolve it?

A. By default, AWS allows you to provision a maximum of 20 instances per Availability Zone. Select a different Availability Zone and retry the failed request.

B. By default, AWS allows you to provision a maximum of 20 instances per region. Select a different region and retry the failed request.

**C. There is a vCPU-based On-Demand Instance limit per region which is why subsequent requests failed. Just submit the limit increase form to AWS and retry the failed requests once approved.**

D. There was an issue with the Amazon EC2 API. Just resend the requests and these will be provisioned successfully.

**Explained**

You are limited to running On-Demand Instances per your vCPU-based On-Demand Instance limit, purchasing 20 Reserved Instances, and requesting Spot Instances per your dynamic Spot limit per region. New AWS accounts may start with limits that are lower than the limits described here.

If you need more instances, complete the Amazon EC2 limit increase request form with your use case, and your limit increase will be considered. Limit increases are tied to the region they were requested for.

=====================================================>

**Question**

A large financial firm in the country has an AWS environment that contains several Reserved EC2 instances hosting a web application that has been decommissioned last week. To save costs, you need to stop incurring charges for the Reserved instances as soon as possible.

What cost-effective steps will you take in this circumstance? (Select TWO.)

**A. Go to the AWS Reserved Instance Marketplace and sell the Reserved instances.**

B.Contact AWS to cancel your AWS subscription.

C. Stop the Reserved instances as soon as possible.

**D. Terminate the Reserved instances as soon as possible to avoid getting billed at the on-demand price when it expires.**

E. Go to the Amazon.com online shopping website and sell the Reserved instances.

=====================================================>

**Question**

A company has a High Performance Computing (HPC) cluster that is composed of EC2 Instances with Provisioned IOPS (io1) volume to process transaction-intensive, low-latency workloads. The Solutions Architect must maintain high IOPS while keeping the latency down by setting the optimal queue length for the volume. The size of each volume is 10 GiB.

Which of the following is the MOST suitable configuration that the Architect should set up?

**A. Set the IOPS to 500 then maintain a low queue length.**

B. Set the IOPS to 800 then maintain a low queue length.

C. Set the IOPS to 400 then maintain a low queue length.

D. Set the IOPS to 600 then maintain a high queue length.

=====================================================>

**Question**

A web application hosted in an Auto Scaling group of EC2 instances in AWS. The application receives a burst of traffic every morning, and a lot of users are complaining about request timeouts. The EC2 instance takes 1 minute to boot up before it can respond to user requests. The cloud architecture must be redesigned to better respond to the changing traffic of the application.

How should the Solutions Architect redesign the architecture?

A. Create a Network Load Balancer with slow-start mode.

B. Create a new launch template and upgrade the size of the instance.

**C. Create a step scaling policy and configure an instance warm-up time condition.**

D. Create a CloudFront distribution and set the EC2 instance as the origin.

=====================================================>

**Question**

A company is planning to launch a High Performance Computing (HPC) cluster in AWS that does Computational Fluid Dynamics (CFD) simulations. The solution should scale-out their simulation jobs to experiment with more tunable parameters for faster and more accurate results. The cluster is composed of Windows servers hosted on t3a.medium EC2 instances. As the Solutions Architect, you should ensure that the architecture provides higher bandwidth, higher packet per second (PPS) performance, and consistently lower inter-instance latencies.

Which is the MOST suitable and cost-effective solution that the Architect should implement to achieve the above requirements?

**A. Enable Enhanced Networking with Elastic Network Adapter (ENA) on the Windows EC2 Instances.**

B. Enable Enhanced Networking with Elastic Fabric Adapter (EFA) on the Windows EC2 Instances.

C. Enable Enhanced Networking with Intel 82599 Virtual Function (VF) interface on the Windows EC2 Instances.

D. Use AWS ParallelCluster to deploy and manage the HPC cluster to provide higher bandwidth, higher packet per second (PPS) performance, and lower inter-instance latencies.

=====================================================>

**Question**

A multinational corporate and investment bank is regularly processing steady workloads of accruals, loan interests, and other critical financial calculations every night from 10 PM to 3 AM on their on-premises data center for their corporate clients. Once the process is done, the results are then uploaded to the Oracle General Ledger which means that the processing should not be delayed or interrupted. The CTO has decided to move its IT infrastructure to AWS to save costs. The company needs to reserve compute capacity in a specific Availability Zone to properly run their workloads.

As the Senior Solutions Architect, how can you implement a cost-effective architecture in AWS for their financial system?

**A. Use On-Demand Capacity Reservations, which provide compute capacity that is always available on the specified recurring schedule.**

B. Use On-Demand EC2 instances which allows you to pay for the instances that you launch and use by the second. Reserve compute capacity in a specific Availability Zone to avoid any interruption.

C. Use Regional Reserved Instances to reserve capacity on a specific Availability Zone and lower down the operating cost through its billing discounts.

D. Use Dedicated Hosts which provide a physical host that is fully dedicated to running your instances, and bring your existing per-socket, per-core, or per-VM software licenses to reduce costs.

=====================================================>

**Question**

A company’s infrastructure consists of Amazon EC2 instances and an Amazon RDS DB instance in a single AWS Region. The company wants to back up its data in a separate Region.

Which solution will meet these requirements with the LEAST operational overhead?

**A. Use AWS Backup to copy EC2 backups and RDS backups to the separate Region.**

B. Use Amazon Data Lifecycle Manager (Amazon DLM) to copy EC2 backups and RDS backups to the separate Region.

C. Create Amazon Machine Images (AMIs) of the EC2 instances. Copy the AMIs to the separate Region. Create a read replica for the RDS DB instance in the separate Region.

D. Create Amazon Elastic Block Store (Amazon EBS) snapshots. Copy the EBS snapshots to the separate Region. Create RDS snapshots. Export the RDS snapshots to Amazon S3. Configure S3 Cross-Region Replication (CRR) to the separate Region.