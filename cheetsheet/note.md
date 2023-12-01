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