## Aurora DB
You can quickly create clones of an Aurora DB by using the database cloning feature. 

In addition, database cloning uses a copy-on-write protocol, in which data is copied only at the time the data changes, either on the source database or the clone database. 

Cloning is much faster than a manual snapshot of the DB cluster.

## Aurora endpoint
Amazon Aurora typically involves a cluster of DB instances instead of a single instance. Each connection is handled by a specific DB instance. When you connect to an Aurora cluster, the host name and port that you specify point to an intermediate handler called an **endpoint**. 

The custom endpoint provides load-balanced database connections based on criteria other than the read-only or read-write capability of the DB instances.
