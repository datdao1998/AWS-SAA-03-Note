**Question**

The engineering team at a retail company is planning to migrate to AWS Cloud from the on-premises data center. The team is evaluating Amazon Relational Database Service (Amazon RDS) as the database tier for its flagship application. The team has hired you as an AWS Certified Solutions Architect Associate to advise on Amazon RDS Multi-AZ capabilities.
Which of the following would you identify as correct for Amazon RDS Multi-AZ? (Select two)

**A. Amazon RDS applies operating system updates by performing maintenance on the standby, then promoting the standby to primary and finally performing maintenance on the old primary, which becomes the new standby**

**B. Amazon RDS automatically initiates a failover to the standby, in case primary database fails for any reason**

C. For automated backups, I/O activity is suspended on your primary database since backups are not taken from standby database

D. To enhance read scalability, a Multi-AZ standby instance can be used to serve read requests

E. Updates to your database Instance are asynchronously replicated across the Availability Zone to the standby in order to keep both in sync

**Explained**

Running a DB instance as a Multi-AZ deployment can further reduce the impact of a maintenance event because Amazon RDS applies operating system updates by following these steps:
* Perform maintenance on the standby.
* Promote the standby to primary.
* Perform maintenance on the old primary, which becomes the new standby.
When you modify the database engine for your DB instance in a Multi-AZ deployment, then Amazon RDS upgrades both the primary and secondary DB instances at the same time. In this case, the database engine for the entire Multi-AZ deployment is shut down during the upgrade.

You also benefit from enhanced database availability when running your DB instance as a Multi-AZ deployment. If an Availability Zone failure or DB instance failure occurs, your availability impact is limited to the time automatic failover takes to complete.

Another implied benefit of running your DB instance as a Multi-AZ deployment is that DB instance failover is automatic and requires no administration. In an Amazon RDS context, this means you are not required to monitor DB instance events and initiate manual DB instance recovery in the event of an Availability Zone failure or DB instance failure.

======================================>

**Question**

A development team runs monthly resource-intensive tests on its general purpose Amazon RDS for MySQL DB instance with Performance Insights enabled. The testing lasts for 48 hours once a month and is the only process that uses the database. The team wants to reduce the cost of running the tests without reducing the compute and memory attributes of the DB instance.
Which solution meets these requirements MOST cost-effectively?

A. Stop the DB instance when tests are completed. Restart the DB instance when required.

B. Use an Auto Scaling policy with the DB instance to automatically scale when tests are completed.

**C. Create a snapshot when tests are completed. Terminate the DB instance and restore the snapshot when required.**

D. Modify the DB instance to a low-capacity instance when tests are completed. Modify the DB instance again when required.

======================================>

**Question**

An application is hosted in an Auto Scaling group of EC2 instances and a Microsoft SQL Server on Amazon RDS. There is a requirement that all in-flight data between your web servers and RDS should be secured.

Which of the following options is the MOST suitable solution that you should implement? (Select TWO.)


**A. Force all connections to your DB instance to use SSL by setting the *rds.force_ssl* parameter to true. Once done, reboot your DB instance.**

B. Configure the security groups of your EC2 instances and RDS to only allow traffic to and from port 443.

**C. Download the Amazon RDS Root CA certificate. Import the certificate to your servers and configure your application to use SSL to encrypt the connection to RDS.**

D. Specify the TDE option in an RDS option group that is associated with that DB instance to enable transparent data encryption (TDE).

E. Enable the IAM DB authentication in RDS using the AWS Management Console

======================================>

**Question**

A company is running an online transaction processing (OLTP) workload on AWS. This workload uses an unencrypted Amazon RDS DB instance in a Multi-AZ deployment. Daily database snapshots are taken from this instance.
What should a solutions architect do to ensure the database and snapshots are always encrypted moving forward?

**A. Encrypt a copy of the latest DB snapshot. Replace existing DB instance by restoring the encrypted snapshot.**

B. Create a new encrypted Amazon Elastic Block Store (Amazon EBS) volume and copy the snapshots to it. Enable encryption on the DB instance.

C. Copy the snapshots and enable encryption using AWS Key Management Service (AWS KMS) Restore encrypted snapshot to an existing DB instance.

D. Copy the snapshots to an Amazon S3 bucket that is encrypted using server-side encryption with AWS Key Management Service (AWS KMS) managed keys (SSE-KMS).

======================================>

**Question**

A company runs its two-tier ecommerce website on AWS. The web tier consists of a load balancer that sends traffic to Amazon EC2 instances. The database tier uses an Amazon RDS DB instance. The EC2 instances and the RDS DB instance should not be exposed to the public internet. The EC2 instances require internet access to complete payment processing of orders through a third-party web service. The application must be highly available.
Which combination of configuration options will meet these requirements? (Choose two.)

**A. Use an Auto Scaling group to launch the EC2 instances in private subnets. Deploy an RDS Multi-AZ DB instance in private subnets.**

B. Configure a VPC with two private subnets and two NAT gateways across two Availability Zones. Deploy an Application Load Balancer in the private subnets.

C. Use an Auto Scaling group to launch the EC2 instances in public subnets across two Availability Zones. Deploy an RDS Multi-AZ DB instance in private subnets.

D. Configure a VPC with one public subnet, one private subnet, and two NAT gateways across two Availability Zones. Deploy an Application Load Balancer in the public subnet.

**E. Configure a VPC with two public subnets, two private subnets, and two NAT gateways across two Availability Zones. Deploy an Application Load Balancer in the public subnets.**