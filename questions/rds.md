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