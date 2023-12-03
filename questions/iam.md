**Question**

A company that is rapidly growing in recent months has been in the process of setting up IAM users on its single AWS Account. A solutions architect has been tasked to handle the user management, which includes granting read-only access to users and denying permissions whenever an IAM user has no MFA setup. New users will be added frequently based on their respective departments.

Which of the following action is the MOST secure way to grant permissions to the new users?

A. Set up IAM roles for each IAM user and associate a permissions boundary that defines the maximum permissions.

B. Create an IAM Role that enforces MFA authentication with the least privilege permission. Set up a corresponding IAM Group for each department. Attach the IAM Role to the IAM Groups.

C. Create a Service Control Policy (SCP) that enforces MFA authentication for each department. Add a trust relationship to every SCP and attach it to each IAM User.

**D. Launch an IAM Group for each department. Create an IAM Policy that enforces MFA authentication with the least privilege permission. Attach the IAM Policy to each IAM Group.**

=====================================================>

**Question**

A company needs to integrate the Lightweight Directory Access Protocol (LDAP) directory service from the on-premises data center to the AWS VPC using IAM. The identity store which is currently being used is not compatible with SAML.

Which of the following provides the most valid approach to implement the integration?

**A. Develop an on-premises custom identity broker application and use STS to issue short-lived AWS credentials.**

B. Use AWS Single Sign-On (SSO) service to enable single sign-on between AWS and your LDAP.

C. Use IAM roles to rotate the IAM credentials whenever LDAP credentials are updated.

D. Use an IAM policy that references the LDAP identifiers and AWS credentials.

=====================================================>

**Question**

A company requires corporate IT governance and cost oversight of all of its AWS resources across its divisions around the world. Their corporate divisions want to maintain administrative control of the discrete AWS resources they consume and ensure that those resources are separate from other divisions.

Which of the following options will support the autonomy of each corporate division while enabling the corporate IT to maintain governance and cost oversight? (Select TWO.)

A. Use AWS Trusted Advisor and AWS Resource Groups Tag Editor

**B. Enable IAM cross-account access for all corporate IT administrators in each child account.**

C. Create separate VPCs for each division within the corporate IT AWS account. Launch an AWS Transit Gateway with equal-cost multipath routing (ECMP) and VPN tunnels for intra-VPC communication.

D. Create separate Availability Zones for each division within the corporate IT AWS account. Improve communication between the two AZs using the AWS Global Accelerator.

**E. Use AWS Consolidated Billing by creating AWS Organizations to link the divisions’ accounts to a parent corporate account.**

=====================================================>

**Question**

A Solutions Architect created a brand new IAM User with a default setting using AWS CLI. This is intended to be used to send API requests to Amazon S3, DynamoDB, Lambda, and other AWS resources of the company’s cloud infrastructure.

Which of the following must be done to allow the user to make API calls to the AWS resources?

A. Enable Multi-Factor Authentication for the user.

B. Assign an IAM Policy to the user to allow it to send API calls.

C. Do nothing as the IAM User is already capable of sending API calls to your AWS resources.

**D. Create a set of Access Keys for the user and attach the necessary permissions.**
