**AWS CloudTrail** is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. 
* With AWS CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. 
* AWS CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command-line tools, and other AWS services.

> By default, CloudTrail event log files are encrypted using Amazon S3 server-side encryption (SSE).

**!!!ALERT**

In general, to analyze any API calls made within an AWS account, AWS CloudTrail is used. 

You can record the actions that are taken by users, roles, or AWS services on Amazon S3 resources and maintain log records for auditing and compliance purposes. To do this, you can use server access logging, AWS CloudTrail logging, or a combination of both. AWS recommends that you use AWS CloudTrail for logging bucket and object-level actions for your Amazon S3 resources.