```
CloudFront provides two ways to send authenticated requests to an Amazon S3 origin: origin access control (OAC) and origin access identity (OAI).

Exam Alert:

Please note that AWS recommends using OAC because it supports:

All Amazon S3 buckets in all AWS Regions, including opt-in Regions launched after December 2022

Amazon S3 server-side encryption with AWS KMS (SSE-KMS)

Dynamic requests (POST, PUT, etc.) to Amazon S3

OAI doesn't work for the scenarios in the preceding list, or it requires extra workarounds in those scenarios. However, you will continue to see answers enlisting OAI as the preferred option in the actual exam as it takes about 6 months/1 year for a new feature to appear in the exam.
```