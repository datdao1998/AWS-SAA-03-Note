**Question** 

A company is building an application in the AWS Cloud. The application will store data in Amazon S3 buckets in two AWS Regions. The company must use an AWS Key Management Service (AWS KMS) customer managed key to encrypt all data that is stored in the S3 buckets. The data in both S3 buckets must be encrypted and decrypted with the same KMS key. The data and the key must be stored in each of the two Regions.
Which solution will meet these requirements with the LEAST operational overhead?

A. Create an S3 bucket in each Region. Configure the S3 buckets to use server-side encryption with Amazon S3 managed encryption keys (SSE-S3). Configure replication between the S3 buckets.

**B. Create a customer managed multi-Region KMS key. Create an S3 bucket in each Region. Configure replication between the S3 buckets. Configure the application to use the KMS key with client-side encryption.**

C. Create a customer managed KMS key and an S3 bucket in each Region. Configure the S3 buckets to use server-side encryption with Amazon S3 managed encryption keys (SSE-S3). Configure replication between the S3 buckets.

D. Create a customer managed KMS key and an S3 bucket in each Region. Configure the S3 buckets to use server-side encryption with AWS KMS keys (SSE-KMS). Configure replication between the S3 buckets

**Explained** AWS KMS supports multi-Region keys, which are AWS KMS keys in different AWS Regions that can be used interchangeably — as though you had the same key in multiple Regions.


=====================================================>

**Question**

A financial services company stores confidential data on an Amazon Simple Storage Service (S3) bucket. The compliance guidelines require that files be stored with server-side encryption. The encryption used must be Advanced Encryption Standard (AES-256) and the company does not want to manage the encryption keys.
Which of the following options represents the most cost-optimal solution for the given use case?

**A. Server-side encryption with Amazon S3 managed keys (SSE-S3)**

B. Server-side encryption with AWS KMS keys (SSE-KMS)

C. Server-side encryption with customer-provided keys (SSE-C)

D. Client Side Encryption

**Explained**

Using Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key employing strong multi-factor encryption. As an additional safeguard, it encrypts the key itself with a master key that it regularly rotates. Amazon S3 server-side encryption uses one of the strongest block ciphers available, 256-bit Advanced Encryption Standard (AES-256), to encrypt your data. There are no additional fees for using server-side encryption with Amazon S3-managed keys (SSE-S3).

=====================================================>

**Question**

A company maintains its business-critical customer data on an on-premises system in an encrypted format. Over the years, the company has transitioned from using a single encryption key to multiple encryption keys by dividing the data into logical chunks. With the decision to move all the data to an Amazon S3 bucket, the company is now looking for a technique to encrypt each file with a different encryption key to provide maximum security to the migrated on-premises data.
How will you implement this requirement without adding the overhead of splitting the data into logical groups?

**A. Configure a single Amazon S3 bucket to hold all data. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data**

B. Store the logically divided data into different Amazon S3 buckets. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data

C. Use Multi-Region keys for client-side encryption in the AWS S3 Encryption Client to generate unique keys for each file of data

D. Configure a single Amazon S3 bucket to hold all data. Use server-side encryption with AWS KMS (SSE-KMS) and use encryption context to generate a different key for each file/object that you store in the S3 bucket

**Explained**

Server-side encryption is the encryption of data at its destination by the application or service that receives it. Amazon S3 encrypts your data at the object level as it writes it to disks in its data centers and decrypts it for you when you access it. When you use server-side encryption with Amazon S3 managed keys (SSE-S3), each object is encrypted with a unique key. As an additional safeguard, it encrypts the key itself with a root key that it regularly rotates.

Note: Amazon S3 now applies server-side encryption with Amazon S3 managed keys (SSE-S3) as the base level of encryption for every bucket in Amazon S3. Starting January 5, 2023, all new object uploads to Amazon S3 will be automatically encrypted at no additional cost and with no impact on performance.

=====================================================>

**Question**

A company helps its customers legally sign highly confidential contracts. To meet the strong industry requirements, the company must ensure that the signed contracts are encrypted using the company's proprietary algorithm. The company is now migrating to AWS Cloud using Amazon Simple Storage Service (Amazon S3) and would like you, the solution architect, to advise them on the encryption scheme to adopt.
What do you recommend?

**A. Client Side Encryption**

B. Server-side encryption with AWS KMS keys (SSE-KMS) 

C. Server-side encryption with Amazon S3 managed keys (SSE-S3)

D. Server-side encryption with customer-provided keys (SSE-C)

**Explained**

Client-side encryption is the act of encrypting your data locally to help ensure its security in transit and at rest. To encrypt your objects before you send them to Amazon S3, use the Amazon S3 Encryption Client. When your objects are encrypted in this manner, your objects aren't exposed to any third party, including AWS. Amazon S3 receives your objects already encrypted; Amazon S3 does not play a role in encrypting or decrypting your objects. You can use both the Amazon S3 Encryption Client and server-side encryption to encrypt your data. When you send encrypted objects to Amazon S3, Amazon S3 doesn't recognize the objects as being encrypted, it only detects typical objects.