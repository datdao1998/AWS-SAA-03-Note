## What is EFS
**Amazon Elastic File System (Amazon EFS)** provides a simple, scalable, fully managed, elastic, NFS file system for use with AWS Cloud services and on-premises resources. 

**Amazon EFS Infrequent Access (EFS IA)** is a storage class that provides price/performance that is cost-optimized for files not accessed every day, with storage prices up to 92% lower compared to Amazon EFS Standard. The EFS IA storage class costs only $0.025/GB-month. To get started with EFS IA, simply enable EFS Lifecycle Management for your file system by selecting a lifecycle policy that matches your needs.

NOTE: Amazon EFS can only transition a file to the IA storage class after 90 days


## EFS Throughput modes
* **Elastic Throughput** (Recommended) – Use the default Elastic Throughput when you have spiky or unpredictable workloads and performance requirements that are difficult to forecast, or when your application drives throughput at an average-to-peak ratio of 5% or less
* **Provisioned Throughput** – Use Provisioned Throughput if you know your workload's performance requirements, or when your application drives throughput at an average-to-peak ratio of 5% or more. 
* **Bursting Throughput** – Use Bursting Throughput when you want throughput that scales with the amount of storage in your file system