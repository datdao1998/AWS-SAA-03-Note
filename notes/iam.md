```
PrincipalOrgId is used by specifying the Principal element in a resource-based policy. You can specify the organization ID in the condition element. When you add and remove accounts, policies that include the aws:PrincipalOrgID key automatically include the correct accounts and don't require manual updating.

For example, the following Amazon S3 bucket policy allows members of any account in the o-xxxxxxxxxxx organization to add an object into the policy-ninja-dev bucket.
```