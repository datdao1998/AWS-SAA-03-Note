**Question**

A company is running an on-premises application backed by a 1TB MySQL 8.0 database. A couple of times each month, the production data is fully copied to a staging database at the request of the analytics team. The team can't work on the staging database until the copy is finished, which takes hours.

Throughout this period, the application experiences intermittent downtimes as well. To expedite the process for the analytics team, a solutions architect must redesign the application's architecture in AWS. The application must also be highly resilient to disruptions.

Which combination of actions best satisfies the given set of requirements while being the most cost-effective? (Select TWO)

**A. Use an Amazon Aurora database with Multi-AZ Replicas**

**B. Clone the production database in the staging environment using Aurora cloning.**

C. Use an Amazon RDS database in a Multi-AZ Deployments configuration

D. Take a manual snapshot and restore it to a database in the staging environment

E. Replicate the production database to a staging database using the mysqldump client utility

**Explained**

The resiliency of an application pertains to its ability to recover from infrastructure or service disruptions. Both Amazon Aurora and Amazon RDS can give you a highly resilient infrastructure by deploying replicas in multiple availability zones. Both database services can perform an automatic failover to a standby instance in the event of failure. However, only Amazon Aurora has the ability to replicate a database in a fast and efficient manner without impacting performance, thanks to its underlying storage system. 

By using Aurora cloning, you can create a new cluster that uses the same Aurora cluster volume and has the same data as the original. The process is designed to be fast and cost-effective. The new cluster with its associated data volume is called a clone.

Creating a clone is faster and more space-efficient than physically copying the data using other techniques, such as restoring from a snapshot like you would in Amazon RDS or using the native mysqldump utility.


==================================>

**Question**

A retail website has intermittent, sporadic, and unpredictable transactional workloads throughout the day that are hard to predict. The website is currently hosted on-premises and is slated to be migrated to AWS. A new relational database is needed that autoscales capacity to meet the needs of the application's peak load and scales back down when the surge of activity is over.

Which of the following option is the MOST cost-effective and suitable database setup in this scenario?

**A. Launch an Amazon Aurora Serverless DB cluster then set the minimum and maximum capacity for the cluster.**

B. Launch an Amazon Redshift data warehouse cluster with Concurrency Scaling.

C. Launch an Amazon Aurora Provisioned DB cluster with burstable performance DB instance class types.

D. Launch a DynamoDB Global table with Auto Scaling enabled.


==================================>

**Question**

A top investment bank is in the process of building a new Forex trading platform. To ensure high availability and scalability, you designed the trading platform to use an Elastic Load Balancer in front of an Auto Scaling group of On-Demand EC2 instances across multiple Availability Zones. For its database tier, you chose to use a single Amazon Aurora instance to take advantage of its distributed, fault-tolerant, and self-healing storage system.

In the event of system failure on the primary database instance, what happens to Amazon Aurora during the failover?

A. Amazon Aurora flips the canonical name record (CNAME) for your DB Instance to point at the healthy replica, which in turn is promoted to become the new primary.

B. Aurora will first attempt to create a new DB Instance in a different Availability Zone of the original instance. If unable to do so, Aurora will attempt to create a new DB Instance in the original Availability Zone in which the instance was first launched.

**C. Aurora will attempt to create a new DB Instance in the same Availability Zone as the original instance and is done on a best-effort basis.**

D. Amazon Aurora flips the A record of your DB Instance to point at the healthy replica, which in turn is promoted to become the new primary.

==================================>

**Question**

A company hosts an application on AWS Lambda functions that are invoked by an Amazon API Gateway API. The Lambda functions save customer data to an Amazon Aurora MySQL database. Whenever the company upgrades the database, the Lambda functions fail to establish database connections until the upgrade is complete. The result is that customer data is not recorded for some of the event.
A solutions architect needs to design a solution that stores customer data that is created during database upgrades.
Which solution will meet these requirements?

A. Provision an Amazon RDS proxy to sit between the Lambda functions and the database. Configure the Lambda functions to connect to the RDS proxy.

B. Increase the run time of the Lambda functions to the maximum. Create a retry mechanism in the code that stores the customer data in the database.

C. Persist the customer data to Lambda local storage. Configure new Lambda functions to scan the local storage to save the customer data to the database.

**D. Store the customer data in an Amazon Simple Queue Service (Amazon SQS) FIFO queue. Create a new Lambda function that polls the queue and stores the customer data in the database.**

==================================>

**Question**

A company is running a multi-tier web application on premises. The web application is containerized and runs on a number of Linux hosts connected to a PostgreSQL database that contains user records. The operational overhead of maintaining the infrastructure and capacity planning is limiting the company's growth. A solutions architect must improve the application's infrastructure.
Which combination of actions should the solutions architect take to accomplish this? (Choose two.)

**A. Migrate the PostgreSQL database to Amazon Aurora.**

B. Migrate the web application to be hosted on Amazon EC2 instances.

C. Set up an Amazon CloudFront distribution for the web application content.

D. Set up Amazon ElastiCache between the web application and the PostgreSQL database.

**E. Migrate the web application to be hosted on AWS Fargate with Amazon Elastic Container Service (Amazon ECS).**

==================================>

**Question**

A company is migrating its on-premises PostgreSQL database to Amazon Aurora PostgreSQL. The on-premises database must remain online and accessible during the migration. The Aurora database must remain synchronized with the on-premises database.
Which combination of actions must a solutions architect take to meet these requirements? (Choose two.)

**A. Create an ongoing replication task.**

B. Create a database backup of the on-premises database.

**C. Create an AWS Database Migration Service (AWS DMS) replication server.**

D. Convert the database schema by using the AWS Schema Conversion Tool (AWS SCT).

E. Create an Amazon EventBridge (Amazon CloudWatch Events) rule to monitor the database synchronization.

==================================>

**Question**

A company stores data in an Amazon Aurora PostgreSQL DB cluster. The company must store all the data for 5 years and must delete all the data after 5 years. The company also must indefinitely keep audit logs of actions that are performed within the database. Currently, the company has automated backups configured for Aurora.

Which combination of steps should a solutions architect take to meet these requirements? (Choose two.)

A. Take a manual snapshot of the DB cluster.

B. Create a lifecycle policy for the automated backups.

C. Configure automated backup retention for 5 years.

**D. Configure an Amazon CloudWatch Logs export for the DB cluster.**

**E. Use AWS Backup to take the backups and to keep the backups for 5 years.** 