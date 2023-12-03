**Question**

A company observes an increase in Amazon EC2 costs in its most recent bill. The billing team notices unwanted vertical scaling of instance types for a couple of EC2 instances. A solutions architect needs to create a graph comparing the last 2 months of EC2 costs and perform an in-depth analysis to identify the root cause of the vertical scaling.
How should the solutions architect generate the information with the LEAST operational overhead?

A. Use AWS Budgets to create a budget report and compare EC2 costs based on instance types.

**B. Use Cost Explorer’s granular filtering feature to perform an in-depth analysis of EC2 costs based on instance types.**

C. Use graphs from the AWS Billing and Cost Management dashboard to compare EC2 costs based on instance types for the last 2 months.

D. Use AWS Cost and Usage Reports to create a report and send it to an Amazon S3 bucket. Use Amazon QuickSight with Amazon S3 as a source to generate an interactive graph based on instance types

========================================>

**Question**

An e-commerce company plans to optimize its disaster recovery configuration using AWS Cloud to minimize operational disruptions during outages or major system maintenance for its on-premises Microsoft SQL Server-based application. The objective is to achieve a recovery point objective (RPO) of 60 seconds or less and a recovery time objective (RTO) of 1 hour.

Which of the following is the MOST cost-effective solution for this scenario?

A. Use Microsoft SQL Server Enterprise with Always On availability groups and set up a multi-site active/active setup between the corporate on-premises application and AWS.

B. Back up SQL Server to AWS Storage Gateway for hybrid storage and fast disaster recovery. Enable fast snapshot restore in Amazon Elastic Block Store (Amazon EBS).

**C. Set up a pilot light strategy using AWS Elastic Disaster Recovery (AWS DRS) to replicate the changes of the on-premises application to AWS**

D. On AWS, implement a warm standby using Amazon RDS for SQL Server database and configure AWS Database Migration Service (AWS DMS) with change data capture (CDC) to sync the data from the on-premises application.