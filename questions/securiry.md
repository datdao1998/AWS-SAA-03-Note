**Question**

An Intelligence Agency developed a missile tracking application that is hosted on both development and production AWS accounts. The Intelligence agency’s junior developer only has access to the development account. She has received security clearance to access the agency’s production account but the access is only temporary and only write access to EC2 and S3 is allowed.

Which of the following allows you to issue short-lived access tokens that act as temporary security credentials to allow access to your AWS resources?

A. All of the given options are correct.

B. Use AWS IAM Identity Center

**C. Use AWS STS**

D. Use AWS Cognito to issue JSON Web Tokens (JWT)

**Explained**

AWS Security Token Service (AWS STS) is the service that you can use to create and provide trusted users with temporary security credentials that can control access to your AWS resources. Temporary security credentials work almost identically to the long-term access key credentials that your IAM users can use.

==============================>

**Question**

A business plans to deploy an application on EC2 instances within an Amazon VPC and is considering adopting a Network Load Balancer to distribute incoming traffic among the instances. A solutions architect needs to suggest a solution that will enable the security team to inspect traffic entering and exiting their VPC.

Which approach satisfies the requirements?

A. Create a firewall at the subnet level using the Amazon Detective service. Inspect the ingress and egress traffic using the VPC Reachability Analyzer.

B. Enable Traffic Mirroring on the Network Load Balancer and forward traffic to the instances. Create a traffic mirror filter to inspect the ingress and egress of data that traverses your Amazon VPC.

C. Use the Network Access Analyzer service on the application’s VPC for inspecting ingress and egress traffic. Create a new Network Access Scope to filter and analyze all incoming and outgoing requests.

**D. Create a firewall using the AWS Network Firewall service at the VPC level then add custom rule groups for inspecting ingress and egress traffic. Update the necessary VPC route tables.**

==============================>

**Question**

A news company is planning to use a Hardware Security Module (CloudHSM) in AWS for secure key storage of their web applications. You have launched the CloudHSM cluster but after just a few hours, a support staff mistakenly attempted to log in as the administrator three times using an invalid password in the Hardware Security Module. This has caused the HSM to be zeroized, which means that the encryption keys on it have been wiped. Unfortunately, you did not have a copy of the keys stored anywhere else.

How can you obtain a new copy of the keys that you have stored on Hardware Security Module?

**A. The keys are lost permanently if you did not have a copy.**

B. Contact AWS Support and they will provide you a copy of the keys.

C. Use the Amazon CLI to get a copy of the keys.

D. Restore a snapshot of the Hardware Security Module.