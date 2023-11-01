## Unversioned, versioning-enabled, and versioning-suspended buckets

1. You enable and suspend versioning at the bucket level. After you version-enable a bucket, it can never return to an unversioned state. But you can suspend versioning on that bucket.

2. Objects that are stored in your bucket before you set the versioning state have a version ID of null. When you enable versioning, existing objects in your bucket do not change. What changes is how Amazon S3 handles the objects in future requests. For more information, see Working with objects in a versioning-enabled bucket.

3. The bucket owner (or any user with appropriate permissions) can suspend versioning to stop accruing object versions. When you suspend versioning, existing objects in your bucket do not change. What changes is how Amazon S3 handles objects in future requests. For more information, see Working with objects in a versioning-suspended bucket.

