**Question**

A company has a fixed set of Amazon EC2 instances inside a VPC in the AWS cloud. The instances run a mission-critical application. In a recent incident, one of the EC2 instances suddenly powered down which affected the availability of the application. To avoid this incident in the future, the management wants to get notified of any upcoming AWS events that may affect these EC2 instances.

Which of the following options is the recommended action to meet the above requirements?

A. Set up an Amazon EventBridge (Amazon CloudWatch Events) rule to check for any status change for Amazon EC2 instances. Set the target to an AWS Lambda function that will send a notification and restart the affected Amazon EC2 instances.

B. Set up an Amazon EventBridge (Amazon CloudWatch Events) rule to check for AWS Service Health Dashboard events that are related to Amazon EC2 instances. To send notifications, set an Amazon SNS topic as a target for the rule.

C. Create an Amazon EventBridge (Amazon CloudWatch Events) rule that is scheduled to run every 24 hours. Set the target to an AWS Lambda function that will check AWS Service Health Dashboard and send notifications for any events that may affect Amazon EC2 instances.

**D. Create an Amazon EventBridge (Amazon CloudWatch Events) rule to check for AWS Personal Health Dashboard events that are related to Amazon EC2 instances. To send notifications, set an Amazon SNS topic as a target for the rule.**

=====================================================>

**Question**

A Solutions Architect is working for a fast-growing startup that just started operations during the past 3 months. They currently have an on-premises Active Directory and 10 computers. To save costs in procuring physical workstations, they decided to deploy virtual desktops for their new employees in a virtual private cloud in AWS. The new cloud infrastructure should leverage the existing security controls in AWS but can still communicate with their on-premises network.

Which set of AWS services will the Architect use to meet these requirements?

A. AWS Directory Services, VPN connection, and AWS Identity and Access Management

B. AWS Directory Services, VPN connection, and ClassicLink

**C. AWS Directory Services, VPN connection, and Amazon Workspaces**

D. AWS Directory Services, VPN connection, and Amazon S3

=====================================================>

**Question**

A research institute has developed simulation software that requires significant computational power. Currently, the software runs on a local server with limited resources, taking several hours to complete each simulation. The server has 32 virtual CPUs (vCPUs) and 256 GiB of memory. The institute plans to migrate the software to AWS. Their objective is to speed up the simulations by running them in parallel.

As a Solutions Architect, which solution will achieve this goal with the LEAST operational overhead?

**A. Utilize AWS Batch to manage the execution of the software.**

B. Consider using Amazon EC2 Spot Instances to run the simulations.

C. Run the simulations using AWS Fargate.

D. Use Lambda functions to process simulation tasks in parallel.

=====================================================>

**Question**

A large company has several applications hosted on hundreds of virtual machines running in its data center. The company wants to take advantage of the scalability and cost-effectiveness of the AWS cloud, so it’s been decided to migrate all its applications to the cloud. Before starting the migration process, the management wants to have an inventory of all its servers and wants the ability to track the migration of each application to the cloud.

Which of the following options is the recommended action to meet the above requirements?

A. Deploy the AWS DataSync agent on the on-premises data center. The data gathered on-site will be stored on an Amazon S3 bucket. Use the AWS Migration Hub console to track the migration of each application.

B. Use AWS Application Migration Service (AWS MGN) and deploy the replication agent on all virtual machines in the data center. Use Amazon QuickSight to visualize the data gathered by the replication agent and track the migration process.

C. Deploy the AWS DataSync agent on the on-premises data center. Data gathered will be stored on an Amazon S3 bucket. Use Amazon QuickSight to visualize the data gathered by the DataSync agent and track the migration process.

**D. Use AWS Application Discovery Service and deploy the discovery connector to the on-premises data center to create an inventory of virtual machines to be migrated. Use the AWS Migration Hub console to track the migration of each application.**

==================================>

**Question**

A solutions architect is formulating a strategy for a startup that needs to transfer 50 TB of on-premises data to Amazon S3. The startup has a slow network transfer speed between its data center and AWS which causes a bottleneck for data migration.

Which of the following should the solutions architect implement?

A. Integrate AWS Storage Gateway File Gateway with the on-premises data center.

B. Enable Amazon S3 Transfer Acceleration on the target S3 bucket.

C. Deploy an AWS Migration Hub Discovery agent in the on-premises data center.

**D. Request an Import Job to Amazon S3 using a Snowball device in the AWS Snowball Console.**

==================================>

**Question**

A company has migrated its containerized workloads into the AWS Cloud. The microservices applications are hosted on Amazon EC2 instances with Docker installed, Amazon Elastic Container Service (Amazon ECS), and newer deployments are hosted on Amazon Elastic Kubernetes Service (Amazon EKS). The company is using open-source tools such as Prometheus and Grafana installed on a virtual machine in its data center for monitoring its applications. The management wants to use the same tools for monitoring its containerized applications in its cloud environment.

Which of the following options is the recommended implementation for this scenario?

A. Export the on-premises VM and upload the image to an Amazon S3 bucket. Use VM Import/Export to import the image and launch it as an Amazon EC2 instance. Reconfigure Prometheus and Grafana to monitor the containerized cloud workloads.

**B. Create a workspace on AWS Manage Service for Prometheus to collect container metrics. Set this workspace as the data source in AWS Managed Grafana for monitoring and data visualization.**

C. Create a new Amazon ECS cluster. Deploy the Prometheus and Grafana containers on this cluster for monitoring containerized workloads. Configure Prometheus for container metrics collection and Grafana for monitoring and data visualization.

D. Create a new workspace AWS Managed Grafana to collect container metrics. Associate this as a data source in Amazon Managed Service for Prometheus. Configure data queries on Prometheus to visualize, monitor, and create alerts for the containerized workloads.

==================================>

**Question**

A FinTech company has been running its compute workload on the AWS Cloud. In order to quickly release the application, the developers have deployed several Amazon EC2 instances, Auto Scaling groups and AWS Lambda functions for the different components of the application stack. After a few weeks of operation, the users are complaining of slow performance in certain components of the application. The QA engineers suspect that the servers are not able to handle the traffic being sent to the application.

Which of the following actions should be taken to verify and resolve the above issue?

A. Use AWS Trusted Advisor and select the cost optimization category to identify overutilized and underutilized resources. Resize the compute resources based on the recommendations.

B. Use AWS CloudWatch to view performance metrics of the compute resources. Create a CloudWatch dashboard to identify overutilized or underutilized resources.

**C. Enable AWS Compute Optimizer to see recommendations on optimal sizing of compute-related resources. Implement changes based on the recommendations.**

D. Use AWS Cost Explorer to gather cost information on all compute-related resources. Increase the size of the instances based on how much budget is allowed by the company.

==================================>

**Question**

A technology company has a suite of container-based web applications and serverless solutions that are hosted in AWS. The Solutions Architect must define a standard infrastructure that will be used across development teams and applications. There are application-specific resources too that change frequently, especially during the early stages of application development. Developers must be able to add supplemental resources to their applications, which are beyond what the architects predefined in the system environments and service templates.

Which of the following should be implemented to satisfy this requirement?

A. Use the Amazon Elastic Container Service (ECS) Anywhere service for deploying container applications and serverless solutions. Configure Prometheus metrics collection on the ECS cluster and use Amazon Managed Service for Prometheus for monitoring frequently-changing resources

B. Set up AWS Control Tower to automate container-based application deployments. Use AWS Config for application-specific resources that change frequently.

C. Use the Amazon EKS Anywhere service for deploying container applications and serverless solutions. Create a service instance for each application-specific resource.

**D. Set up AWS Proton for deploying container applications and serverless solutions. Create components from the AWS Proton console and attach them to their respective service instance.**

==================================>

**Question**

A company is designing a customized text messaging service that targets its mobile app users. As part of its multi-engagement marketing campaign, a company needs to send a one-time confirmation message to all of its subscribers using Short Message Service (SMS). The solutions architect must design the system to allow a subscriber to reply to the SMS messages.

The customer responses must be kept for an entire year for analysis and targeted sale promotions. In addition, the SMS responses must also be collected, processed, and analyzed in near-real-time.

Which solution will meet these requirements with the LEAST operational overhead?

A. Create a new topic in Amazon Simple Notification Service (Amazon SNS) and an Amazon Kinesis data stream configured with all its default settings. Send SMS messages using Amazon SNS. Integrate the Kinesis data stream to the SNS topic for data collection, archiving, and analysis.

B. Launch a new Amazon Simple Queue Service (Amazon SQS) queue to send out SMS messages. Use AWS Step Functions and AWS Lambda to collect, process, and analyze responses. Store the data to Amazon S3 Glacier Instant Retrieval.

**C. Create an Amazon Pinpoint journey for the multi-engagement SMS marketing campaign and an Amazon Kinesis Data Stream for analysis. Configure Amazon Pinpoint to send events to the Kinesis data stream for collection, processing, and analysis. Set the retention period of the Kinesis data stream to 365 days.**

D. Set up an Amazon Connect contact flow to send the confirmation SMS messages to the mobile app users. Deploy an AWS Lambda function to process and analyze the responses. Store the data to Amazon S3 Glacier Flexible Retrieval

==================================>

**Question**

A company has a web application that is based on Java and PHP. The company plans to move the application from on premises to AWS. The company needs the ability to test new site features frequently. The company also needs a highly available and managed solution that requires minimum operational overhead.

Which solution will meet these requirements?

A. Create an Amazon S3 bucket. Enable static web hosting on the S3 bucket. Upload the static content to the S3 bucket. Use AWS Lambda to process all dynamic content.

**B. Deploy the web application to an AWS Elastic Beanstalk environment. Use URL swapping to switch between multiple Elastic Beanstalk environments for feature testing.**

C. Deploy the web application to Amazon EC2 instances that are configured with Java and PHP. Use Auto Scaling groups and an Application Load Balancer to manage the website’s availability.

D. Containerize the web application. Deploy the web application to Amazon EC2 instances. Use the AWS Load Balancer Controller to dynamically route traffic between containers that contain the new site features for testing.

==================================>

**Question**

A company has a Microsoft .NET application that runs on an on-premises Windows Server. The application stores data by using an Oracle Database Standard Edition server. The company is planning a migration to AWS and wants to minimize development changes while moving the application. The AWS application environment should be highly available.

Which combination of actions should the company take to meet these requirements? (Choose two.)

A. Refactor the application as serverless with AWS Lambda functions running .NET Core.

**B. Rehost the application in AWS Elastic Beanstalk with the .NET platform in a Multi-AZ deployment.**

C. Replatform the application to run on Amazon EC2 with the Amazon Linux Amazon Machine Image (AMI).

D. Use AWS Database Migration Service (AWS DMS) to migrate from the Oracle database to Amazon DynamoDB in a Multi-AZ deployment.

**E. Use AWS Database Migration Service (AWS DMS) to migrate from the Oracle database to Oracle on Amazon RDS in a Multi-AZ deployment.**