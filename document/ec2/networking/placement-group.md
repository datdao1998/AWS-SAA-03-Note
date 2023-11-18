# Placement group strategies
* **Cluster** – packs instances close together inside an Availability Zone. This strategy enables workloads to achieve the low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of high-performance computing (HPC) applications.
* **Partition** – spreads your instances across logical partitions such that groups of instances in one partition do not share the underlying hardware with groups of instances in different partitions. This strategy is typically used by large distributed and replicated workloads, such as Hadoop, Cassandra, and Kafka.
* **Spread** – strictly places a small group of instances across distinct underlying hardware to reduce correlated failures.

## Cluster placement groups
* A **cluster placement group** is a logical grouping of instances within a single Availability Zone. A cluster placement group can span peered virtual private networks (VPCs) in the same Region.
* Cluster placement groups are recommended for applications that benefit from low network latency, high network throughput, or both

## Partition placement groups
* **Partition placement groups** help reduce the likelihood of correlated hardware failures for your application. When using partition placement groups:
    * Amazon EC2 divides each group into logical segments called partitions. 
    * Amazon EC2 ensures that each partition within a placement group has its own set of racks. Each rack has its own network and power source. 
    * No two partitions within a placement group share the same racks, allowing you to isolate the impact of hardware failure within your application.
* Partition placement groups can be used to deploy large distributed and replicated workloads, such as HDFS, HBase, and Cassandra, across distinct racks. 
* A partition placement group can have partitions in multiple Availability Zones in the same Region. ***A partition placement group can have a maximum of 7 partitions per Availability Zone***

## Spread placement groups
* A spread placement group is a group of instances that are each placed on distinct hardware.
* Spread placement groups are recommended for applications that have a small number of critical instances that should be kept separate from each other. 
* A rack spread placement group can span multiple Availability Zones in the same Region. ***For rack spread level placement groups, you can have a maximum of seven running instances per Availability Zone per group.***
