**Question**

A company is in the process of migrating their applications to AWS. One of their systems requires a database that can scale globally and handle frequent schema changes. The application should not have any downtime or performance issues whenever there is a schema change in the database. It should also provide a low latency response to high-traffic queries.

Which is the most suitable database solution to use to achieve this requirement?

A. An Amazon RDS instance in Multi-AZ Deployments configuration

B. An Amazon Aurora database with Read Replicas

**C. Amazon DynamoDB**

D. Redshift

**Explained**

Before we proceed in answering this question, we must first be clear with the actual definition of a “schema“. Basically, the english definition of a schema is: a representation of a plan or theory in the form of an outline or model.

Just think of a schema as the “structure” or a “model” of your data in your database. Since the scenario requires that the schema, or the structure of your data, changes frequently, then you have to pick a database which provides a non-rigid and flexible way of adding or removing new types of data. This is a classic example of choosing between a relational database and non-relational (NoSQL) database.

========================================>

**Question**

A GraphQL API hosted is hosted in an Amazon EKS cluster with Fargate launch type and deployed using AWS SAM. The API is connected to an Amazon DynamoDB table with an Amazon DynamoDB Accelerator (DAX) as its data store. Both resources are hosted in the us-east-1 region.

The AWS IAM authenticator for Kubernetes is integrated into the EKS cluster for role-based access control (RBAC) and cluster authentication. A solutions architect must improve network security by preventing database calls from traversing the public internet. An automated cross-account backup for the DynamoDB table is also required for long-term retention.

Which of the following should the solutions architect implement to meet the requirement?

**A. Create a DynamoDB gateway endpoint. Associate the endpoint to the appropriate route table. Use AWS Backup to automatically copy the on-demand DynamoDB backups to another AWS account for disaster recovery.**

B. Create a DynamoDB interface endpoint. Associate the endpoint to the appropriate route table. Enable Point-in-Time Recovery (PITR) to restore the DynamoDB table to a particular point in time on the same or a different AWS account.

C. Create a DynamoDB gateway endpoint. Set up a Network Access Control List (NACL) rule that allows outbound traffic to the dynamodb.us-east-1.amazonaws.com gateway endpoint. Use the built-in on-demand DynamoDB backups for cross-account backup and recovery.

D. Create a DynamoDB interface endpoint. Set up a stateless rule using AWS Network Firewall to control all outbound traffic to only use the dynamodb.us-east-1.amazonaws.com endpoint. Integrate the DynamoDB table with Amazon Timestream to allow point-in-time recovery from a different AWS account.

========================================>

**Question**

A company currently has an Augment Reality (AR) mobile game that has a serverless backend. It is using a DynamoDB table which was launched using the AWS CLI to store all the user data and information gathered from the players and a Lambda function to pull the data from DynamoDB. The game is being used by millions of users each day to read and store data.

How would you design the application to improve its overall performance and make it more scalable while keeping the costs low? (Select TWO)

**A. Enable DynamoDB Accelerator (DAX) and ensure that the Auto Scaling is enabled and increase the maximum provisioned read and write capacity.**

B. Configure CloudFront with DynamoDB as the origin; cache frequently accessed data on the client device using ElastiCache.

C. Use AWS IAM Identity Center to authenticate users and have them directly access DynamoDB using single sign-on. Manually set the provisioned read and write capacity to a higher RCU and WCU.

**D. Use API Gateway in conjunction with Lambda and turn on the caching on frequently accessed data and enable DynamoDB global replication.**

E. Since Auto Scaling is enabled by default, the provisioned read and write capacity will adjust automatically. Also enable DynamoDB Accelerator (DAX) to improve the performance from milliseconds to microseconds.