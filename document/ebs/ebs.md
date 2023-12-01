# Amazon Data Lifecycle Manager

You can use Amazon Data Lifecycle Manager (Amazon DLM) to automate the creation, retention, and deletion of snapshots taken to back up your Amazon EBS volumes. Automating snapshot management helps you to:

– Protect valuable data by enforcing a regular backup schedule.

– Retain backups as required by auditors or internal compliance.

– Reduce storage costs by deleting outdated backups.

Combined with the monitoring features of Amazon CloudWatch Events and AWS CloudTrail, Amazon DLM provides a complete backup solution for EBS volumes at no additional cost.


# Encrypted volume
When you create an encrypted EBS volume and attach it to a supported instance type, the following types of data are encrypted:

* Data at rest inside the volume

* All data moving between the volume and the instance

* All snapshots created from the volume

* All volumes created from those snapshots