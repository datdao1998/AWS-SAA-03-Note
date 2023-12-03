```
gRPC protocol is at Layer 7 of the OSI
```

```
The FTP protocol uses TCP via ports 20 and 21
```

```
With AWS DataSync, you can transfer data from on-premises directly to Amazon S3 Glacier Deep Archive. 
You don’t have to configure the S3 lifecycle policy and wait for 30 days to move the data to Glacier Deep Archive.
```

```
An organization plans to use an AWS Direct Connect connection to establish a dedicated connection between its on-premises network and AWS. The organization needs to launch a fully managed solution that will automate and accelerate the replication of data to and from various AWS storage services.

-> in the scenario, you need to accelerate the replication of data, and not establish a hybrid cloud storage architecture. AWS Storage Gateway only supports a few AWS storage services as a target based on the type of gateway that you launched. AWS DataSync is more suitable in automating and accelerating online data transfers to a variety of AWS storage services.
```

```
If the Auto Scaling group (ASG) is using EC2 as the health check type and the Application Load Balancer (ALB) is using its in-built health check, there may be a situation where 
* The ALB health check fails because the health check pings fail to receive a response from the instance.
* At the same time, ASG health check can come back as successful because it is based on EC2 based health check.

Therefore, in this scenario, the ALB will remove the instance from its inventory, however, the Auto Scaling Group will fail to provide the replacement instance.
```

```
NACLs are stateless
Security groups are stateful
```

```
Both AWS Storage Gateway and AWS DataSync can send data from your on-premises data center to AWS and vice versa. 
* AWS Storage Gateway is more suitable to be used in integrating your storage services by replicating your data
* AWS DataSync is better for workloads that require you to move or migrate your data.
```

```
Objects must be stored for at least 30 days in the current storage class before you can transition them to STANDARD_IA or ONEZONE_IA.
```

```
IAM roles are global services that are available to all regions
```

```
Amazon ECS doesn’t support resource-based policies.
```

```
You cannot set up an Active-Active Failover with One Primary and One Secondary Resource. Remember that an Active-Active Failover uses all available resources all the time without a primary nor a secondary resource.
```

```
CloudFront geo-restriction feature is primarily used to prevent users in specific geographic locations from accessing content that you’re distributing through a CloudFront web distribution. 

It does not let you choose the resources that serve your traffic based on the geographic location of your users, unlike the Geolocation routing policy in Route 53.
```

```
Reserved Instances that applied to terminated instances are still billed until the end of their term according to their payment option.
```

```
No ready to use Cloudwatch metrics

1. Memory utilization
2. Disk swap utilization
3. Disk space utilization
4. Page file utilization
5. Log collection
```

```
Amazon QuickSight only support users(standard version) and groups (enterprise version). users and groups only exists without QuickSight. QuickSight don't support IAM. 
```

```
Kinesis Data Firehose currently supports Amazon S3, Amazon Redshift, Amazon OpenSearch Service, Splunk, Datadog, NewRelic, Dynatrace, Sumologic, LogicMonitor, MongoDB, and HTTP End Point as destinations.
```

```
You can use CloudFront to deliver video on demand (VOD) or live streaming video using any HTTP origin
```

```
WAF - can't support NLB and its supports API Gateway
```

```
RDS Multi-AZ = Synchronous = Disaster Recovery (DR)
Read Replica = Asynchronous = High Availability
```

```
Whenever you see SFTP , FTP look for "Transfer" in options available
```