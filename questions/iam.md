**Question**

A company that is rapidly growing in recent months has been in the process of setting up IAM users on its single AWS Account. A solutions architect has been tasked to handle the user management, which includes granting read-only access to users and denying permissions whenever an IAM user has no MFA setup. New users will be added frequently based on their respective departments.

Which of the following action is the MOST secure way to grant permissions to the new users?

A. Set up IAM roles for each IAM user and associate a permissions boundary that defines the maximum permissions.

B. Create an IAM Role that enforces MFA authentication with the least privilege permission. Set up a corresponding IAM Group for each department. Attach the IAM Role to the IAM Groups.

C. Create a Service Control Policy (SCP) that enforces MFA authentication for each department. Add a trust relationship to every SCP and attach it to each IAM User.

**D. Launch an IAM Group for each department. Create an IAM Policy that enforces MFA authentication with the least privilege permission. Attach the IAM Policy to each IAM Group.**