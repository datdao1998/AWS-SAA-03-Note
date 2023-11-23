**Question** A company is developing a document management application on AWS. The application runs on Amazon EC2 instances in multiple Availability Zones (AZs). The company requires the document store to be highly available and the documents need to be returned immediately when requested. The engineering team has configured the application to use Amazon Elastic Block Store (Amazon EBS) to store the documents but the team is willing to consider other options to meet the availability requirement.

As a solutions architect, which of the following will you recommend?

**A. Set up Amazon EBS as the Amazon EC2 instance root volume and then configure the application to use Amazon S3 as the document store**

B. Create snapshots for the Amazon EBS volumes regularly and then build new volumes using those snapshots in additional Availability Zones

C. Set up Amazon EBS as the Amazon EC2 instance root volume and then configure the application to use Amazon S3 Glacier as the document store

D. Provision at least three Provisioned IOPS Amazon EBS volumes for the Amazon EC2 instances and then mount these volumes to the Amazon EC2 instances in a RAID 5 configuration

**Explained**

Instances that use Amazon EBS for the root device automatically have an Amazon EBS volume attached. When you launch an Amazon EBS-backed instance, AWS creates an Amazon EBS volume for each Amazon EBS snapshot referenced by the AMI you use. An Amazon EBS-backed instance can be stopped and later restarted without affecting data stored in the attached volumes.

Amazon S3 provides access to reliable, fast, and inexpensive data storage infrastructure. It is designed to make web-scale computing easier by enabling you to store and retrieve any amount of data, at any time, from within Amazon EC2 or anywhere on the web. S3 is highly available and can be configured to work as a document store for the given use case.

=====================================================>

**Question**

An application is hosted on multiple Amazon EC2 instances in the same Availability Zone (AZ). The engineering team wants to set up shared data access for these Amazon EC2 instances using Amazon EBS Multi-Attach volumes.
Which Amazon EBS volume type is the correct choice for these Amazon EC2 instances?

**A. Provisioned IOPS SSD Amazon EBS volumes**

B. General-purpose SSD-based Amazon EBS volumes

C. Throughput Optimized HDD Amazon EBS volumes

D. Cold HDD Amazon EBS volumes

**Explained** 

Amazon EBS Multi-Attach enables you to attach a single Provisioned IOPS SSD (io1 or io2) volume to multiple instances that are in the same Availability Zone. You can attach multiple Multi-Attach enabled volumes to an instance or set of instances. Each instance to which the volume is attached has full read and write permission to the shared volume. Multi-Attach makes it easier for you to achieve higher application availability in clustered Linux applications that manage concurrent write operations.
Multi-Attach is supported exclusively on Provisioned IOPS SSD volumes.