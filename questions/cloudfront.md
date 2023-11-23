**Question**

A digital media streaming company wants to use Amazon CloudFront to distribute its content only to its service subscribers. As a solutions architect, which of the following solutions would you suggest to deliver restricted content to the bona fide end users? (Select two)

**A. Use Amazon CloudFront signed URLs**

**B. Use Amazon CloudFront signed cookies**

C. Require HTTPS for communication between Amazon CloudFront and your custom origin

D. Require HTTPS for communication between Amazon CloudFront and your S3 origin

E. Forward HTTPS requests to the origin server by using the ECDSA or RSA ciphers

**Explained**

Many companies that distribute content over the internet want to restrict access to documents, business data, media streams, or content that is intended for selected users, for example, users who have paid a fee.
To securely serve this private content by using Amazon CloudFront, you can do the following:
* Require that your users access your private content by using special Amazon CloudFront signed URLs or signed cookies.
* A signed URL includes additional information, for example, expiration date and time, that gives you more control over access to your content. So this is a correct option.

Amazon CloudFront signed cookies allow you to control who can access your content when you don't want to change your current URLs or when you want to provide access to multiple restricted files, for example, all of the files in the subscribers' area of a website. So this is also a correct option.