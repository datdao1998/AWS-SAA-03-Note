**Question**

An Intelligence Agency developed a missile tracking application that is hosted on both development and production AWS accounts. The Intelligence agency’s junior developer only has access to the development account. She has received security clearance to access the agency’s production account but the access is only temporary and only write access to EC2 and S3 is allowed.

Which of the following allows you to issue short-lived access tokens that act as temporary security credentials to allow access to your AWS resources?

A. All of the given options are correct.

B. Use AWS IAM Identity Center

**C. Use AWS STS**

D. Use AWS Cognito to issue JSON Web Tokens (JWT)

**Explained**

AWS Security Token Service (AWS STS) is the service that you can use to create and provide trusted users with temporary security credentials that can control access to your AWS resources. Temporary security credentials work almost identically to the long-term access key credentials that your IAM users can use.