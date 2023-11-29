## S3 Access Point
Amazon S3 Access Points are named network endpoints with dedicated access policies that describe how data can be accessed using that endpoint. Access Points are attached to buckets that you can use to perform S3 object operations, such as GetObject and PutObject. Access Points simplify managing data access at scale for shared datasets in Amazon S3.

## Access control lists (ACLs)
You can use ACLs to grant read and write permissions to authorized users for individual buckets and objects. Each bucket and object has an ACL attached to it as a subresource. The ACL defines which AWS accounts or groups are granted access and the type of access. ACLs are an access control mechanism that predates IAM

## S3 Object Lock
**Amazon S3 Object Lock** is an Amazon S3 feature that allows you to store objects using a write once, read many (WORM) model. 

You can use WORM protection for scenarios where it is imperative that data is not changed or deleted after it has been written. Whether your business has a requirement to satisfy compliance regulations in the financial or healthcare sector, or you simply want to capture a golden copy of business records for later auditing and reconciliation, Amazon S3 Object Lock is the right tool for you. 

**Object Lock** can help prevent objects from being deleted or overwritten for a fixed amount of time or indefinitely.

**Object Lock** provides two ways to manage object retention: retention periods and legal holds. An object version can have a retention period, a legal hold, or both.
1. **Retention period** – A retention period specifies a fixed period of time during which an object remains locked. You can set a default retention period on an S3 bucket. You can also set a unique retention period for individual objects.
    
    S3 Object Lock provides two retention modes:
    * ***Governance mode***: Protect objects against being deleted by most users, but you can still grant some users permission to alter the retention settings or delete the object if necessary.

    * ***Compliance mode***: A protected object version can’t be overwritten or deleted by any user, including the root user in your AWS account

2. **Legal hold** – A legal hold provides the same protection as a retention period, but it has no expiration date. Instead, a legal hold remains in place until you explicitly remove it. Legal holds are independent from retention periods and are placed on individual objects.