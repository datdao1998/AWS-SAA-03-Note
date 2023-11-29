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

==========================================>

**Question**

A popular social media website uses a CloudFront web distribution to serve their static contents to their millions of users around the globe. They are receiving a number of complaints recently that their users take a lot of time to log into their website. There are also occasions when their users are getting HTTP 504 errors. You are instructed by your manager to significantly reduce the user’s login time to further optimize the system.

Which of the following options should you use together to set up a cost-effective solution that can improve your application’s performance? (Select TWO.)

A. Use multiple and geographically disperse VPCs to various AWS regions then create a transit VPC to connect all of your resources. In order to handle the requests faster, set up Lambda functions in each region using the AWS Serverless Application Model (SAM) service.

B. Configure your origin to add a Cache-Control max-age directive to your objects, and specify the longest practical value for max-age to increase the cache hit ratio of your CloudFront distribution.

**C. Set up an origin failover by creating an origin group with two origins. Specify one as the primary origin and the other as the second origin which CloudFront automatically switches to when the primary origin returns specific HTTP status code failure responses.**

D. Deploy your application to multiple AWS regions to accommodate your users around the world. Set up a Route 53 record with latency routing policy to route incoming traffic to the region that provides the best latency to the user.

**E. Customize the content that the CloudFront web distribution delivers to your users using Lambda@Edge, which allows your Lambda functions to execute the authentication process in AWS locations closer to the users.**