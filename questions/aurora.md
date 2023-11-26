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