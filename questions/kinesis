**Question**

A Big Data analytics company is using a fleet of Amazon EC2 instances to ingest Internet-of-Things (IoT) data from various data sources. The data is in JSON format and ingestion rates can be as high as 1 MB/s. When an EC2 instance is restarted, the in-flight data is lost. The analytics team at the company wants to store as well as query the ingested data in near-real-time.
Which of the following solutions provides near-real-time data querying that is scalable with minimal data loss?

**A. Capture data in Amazon Kinesis Data Firehose with Amazon Redshift as the destination. Use Amazon Redshift to query the data**

B. Capture data in an Amazon EC2 instance store and then publish this data to Amazon Kinesis Data Firehose with Amazon S3 as the destination. Use Amazon Athena to query the data

C. Capture data in an Amazon EBS volume and then publish this data to Amazon ElastiCache for Redis. Subscribe to the Redis channel to query the data

D. Capture data in Amazon Kinesis Data Streams. Use Amazon Kinesis Data Analytics to query and analyze this streaming data in real-time

**Explained**

Amazon Kinesis Data Firehose is the easiest way to reliably load streaming data into data lakes, data stores, and analytics services. It can capture, transform, and deliver streaming data to Amazon S3, Amazon Redshift, Amazon Elasticsearch Service, generic HTTP endpoints, and service providers like Datadog, New Relic, MongoDB, and Splunk.

Amazon Kinesis Data Firehose is the easiest way to capture, transform, and load streaming data into Redshift for near real-time analytics. It is also an auto-scaling solution as there is no need to provision any shards like Kinesis Data Streams.

Amazon Redshift allows you to run complex analytic queries against petabytes of structured data, using sophisticated query optimization, columnar storage on high-performance local disks, and massively parallel query execution. Most results come back in seconds.