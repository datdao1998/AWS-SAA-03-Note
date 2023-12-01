**Question** 

A company has a production workload that runs on 1,000 Amazon EC2 Linux instances. The workload is powered by third-party software. The company needs to patch the third-party software on all EC2 instances as quickly as possible to remediate a critical security vulnerability.
What should a solutions architect do to meet these requirements?

A. Create an AWS Lambda function to apply the patch to all EC2 instances.

B. Configure AWS Systems Manager Patch Manager to apply the patch to all EC2 instances.

C. Schedule an AWS Systems Manager maintenance window to apply the patch to all EC2 instances.

**D. Use AWS Systems Manager Run Command to run a custom command that applies the patch to all EC2 instances.**

**Explained** Run Command allows you to automate common administrative tasks and perform one-time configuration changes at scale.

=====================================================>

**Question**

A company runs a multi-tier web application in the AWS Cloud. The application tier is hosted on Amazon EC2 instances and the backend database is hosted on an Amazon Aurora for MySQL DB cluster. For security compliance, all of the application variables such as DB hostnames, environment settings, product keys, and database passwords must be stored securely with encryption.

Which of the following options is the most cost-effective solution to meet the requirements?

A. Store the values by creating secrets in AWS Secrets Manager. Use AWS Key Management Service (AWS KMS) for the encryption. Update the application to retrieve the value of the secrets.

B. Store the values as key-value pairs in AWS Systems Manager OpsCenter. By default, the key-value pairs will be encrypted at rest. Configure the application to retrieve the variables when it starts.

**C. Store the values by creating SecureString type parameters in AWS Systems Manager Parameter Store. Use AWS Key Management Service (AWS KMS) for the encryption. Update the application to retrieve the parameter values.**

D. Store the values in a file saved in an Amazon S3 bucket. Enable encryption on the Amazon S3 bucket. Configure the application to download the file contents when it starts.

**Explained**

It is possible to store encrypted parameters on Secrets Manager, however, there is a cost associated with using this service. If you are storing mostly application parameters, then the Systems Manager Parameter Store is a better fit.

=====================================================>

**Question**

A startup launched a fleet of on-demand EC2 instances to host a massively multiplayer online role-playing game (MMORPG). The EC2 instances are configured with Auto Scaling and AWS Systems Manager. 

What can be used to configure the EC2 instances without having to establish an RDP or SSH connection to each instance?

A. AWS Config

B. AWS CodePipeline

**C. Run Command**

D. EC2Config