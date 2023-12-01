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