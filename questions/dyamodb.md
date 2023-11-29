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