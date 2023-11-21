## Cross-zone load balancing
By default, cross-zone load balancing is 
* **Enabled for Application Load Balancer** 
* **Disabled for Network Load Balancer**

When cross-zone load balancing is enabled, each load balancer node distributes traffic across the registered targets in all the enabled Availability Zones. When cross-zone load balancing is disabled, each load balancer node distributes traffic only across the registered targets in its Availability Zone.

## Amazon Aurora Serverless
Amazon Aurora Serverless is an on-demand, auto-scaling configuration for Amazon Aurora (MySQL-compatible and PostgreSQL-compatible editions), where the database will automatically start up, shut down, and scale capacity up or down based on your application's needs.

 It enables you to run your database in the cloud without managing any database instances. It's a simple, cost-effective option for infrequent, intermittent, or unpredictable workloads. 
 
 The database design for an OLTP application fits the relational model, therefore you can infer an OLTP system as a Relational Database.

