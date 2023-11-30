**Question**

A startup has multiple AWS accounts that are assigned to its development teams. Since the company is projected to grow rapidly, the management wants to consolidate all of its AWS accounts into a multi-account setup. To simplify the login process on the AWS accounts, the management wants to utilize its existing directory service for user authentication

Which combination of actions should a solutions architect recommend to meet these requirements? (Select TWO.)

**A. Configure AWS IAM Identity Center (AWS Single Sign-On) for the organization and integrate it with the company’s directory service using the Active Directory Connector**

B. Create an identity pool on Amazon Cognito and configure it to use the company’s directory service. Configure AWS IAM Identity Center (AWS Single Sign-On) to accept Cognito authentication.

**C. On the master account, use AWS Organizations to create a new organization with all features turned on. Invite the child accounts to this new organization.**

D. On the master account, use AWS Organizations to create a new organization with all features turned on. Enable the organization’s external authentication and point it to use the company’s directory service.

E. Create Service Control Policies (SCP) in the organization to manage the child accounts. Configure AWS IAM Identity Center (AWS Single Sign-On) to use AWS Directory Service.