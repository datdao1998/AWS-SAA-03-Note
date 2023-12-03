**Question**

A startup has multiple AWS accounts that are assigned to its development teams. Since the company is projected to grow rapidly, the management wants to consolidate all of its AWS accounts into a multi-account setup. To simplify the login process on the AWS accounts, the management wants to utilize its existing directory service for user authentication

Which combination of actions should a solutions architect recommend to meet these requirements? (Select TWO.)

**A. Configure AWS IAM Identity Center (AWS Single Sign-On) for the organization and integrate it with the company’s directory service using the Active Directory Connector**

B. Create an identity pool on Amazon Cognito and configure it to use the company’s directory service. Configure AWS IAM Identity Center (AWS Single Sign-On) to accept Cognito authentication.

**C. On the master account, use AWS Organizations to create a new organization with all features turned on. Invite the child accounts to this new organization.**

D. On the master account, use AWS Organizations to create a new organization with all features turned on. Enable the organization’s external authentication and point it to use the company’s directory service.

E. Create Service Control Policies (SCP) in the organization to manage the child accounts. Configure AWS IAM Identity Center (AWS Single Sign-On) to use AWS Directory Service.

=====================================================>

**Question**

A company uses AWS Organizations to create dedicated AWS accounts for each business unit to manage each business unit's account independently upon request. The root email recipient missed a notification that was sent to the root user email address of one account. The company wants to ensure that all future notifications are not missed. Future notifications must be limited to account administrators.
Which solution will meet these requirements?

A. Configure the company’s email server to forward notification email messages that are sent to the AWS account root user email address to all users in the organization.

**B. Configure all AWS account root user email addresses as distribution lists that go to a few administrators who can respond to alerts. Configure AWS account alternate contacts in the AWS Organizations console or programmatically.**

C. Configure all AWS account root user email messages to be sent to one administrator who is responsible for monitoring alerts and forwarding those alerts to the appropriate groups.

D. Configure all existing AWS accounts and all newly created accounts to use the same root user email address. Configure AWS account alternate contacts in the AWS Organizations console or programmatically.

=====================================================>

**Question**

A security team wants to limit access to specific services or actions in all of the team’s AWS accounts. All accounts belong to a large organization in AWS Organizations. The solution must be scalable and there must be a single point where permissions can be maintained.

What should a solutions architect do to accomplish this?

A. Create an ACL to provide access to the services or actions.

B. Create a security group to allow accounts and attach it to user groups.

C. Create cross-account roles in each account to deny access to the services or actions.

**D. Create a service control policy in the root organizational unit to deny access to the services or actions.**