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

==========================================>

**Question**

A company has a web application that uses Amazon CloudFront to distribute its images, videos, and other static contents stored in its S3 bucket to its users around the world. The company has recently introduced a new member-only access feature to some of its high-quality media files. There is a requirement to provide access to multiple private media files only to their paying subscribers without having to change their current URLs.

Which of the following is the most suitable solution that you should implement to satisfy this requirement?

A. Configure your CloudFront distribution to use Field-Level Encryption to protect your private data and only allow access to members.

**B. Use Signed Cookies to control who can access the private files in your CloudFront distribution by modifying your application to determine whether a user should have access to your content. For members, send the required Set-Cookie headers to the viewer which will unlock the content only to them.**

C. Create a Signed URL with a custom policy which only allows the members to see the private files.

D. Configure your CloudFront distribution to use Match Viewer as its Origin Protocol Policy which will automatically match the user request. This will allow access to the private content if the request is a paying member and deny it if it is not a member.

==========================================>

**Question**

A company has clients all across the globe that access product files stored in several S3 buckets, which are behind each of their own CloudFront web distributions. They currently want to deliver their content to a specific client, and they need to make sure that only that client can access the data. Currently, all of their clients can access their S3 buckets directly using an S3 URL or through their CloudFront distribution. The Solutions Architect must serve the private content via CloudFront only, to secure the distribution of files.

Which combination of actions should the Architect implement to meet the above requirements? (Select TWO.)

**A. Restrict access to files in the origin by creating an origin access identity (OAI) and give it permission to read the files in the bucket.**

B. Enable the Origin Shield feature of the Amazon CloudFront distribution to protect the files from unauthorized access.

C. Use S3 pre-signed URLs to ensure that only their client can access the files. Remove permission to use Amazon S3 URLs to read the files for anyone else.

**D. Require the users to access the private content by using special CloudFront signed URLs or signed cookies.**

E. Create a custom CloudFront function to check and ensure that only their clients can access the files.

==========================================>

**Question**

A global company hosts its web application on Amazon EC2 instances behind an Application Load Balancer (ALB). The web application has static data and dynamic data. The company stores its static data in an Amazon S3 bucket. The company wants to improve performance and reduce latency for the static data and dynamic data. The company is using its own domain name registered with Amazon Route 53.
What should a solutions architect do to meet these requirements?

**A. Create an Amazon CloudFront distribution that has the S3 bucket and the ALB as origins. Configure Route 53 to route traffic to the CloudFront distribution.**

B. Create an Amazon CloudFront distribution that has the ALB as an origin. Create an AWS Global Accelerator standard accelerator that has the S3 bucket as an endpoint Configure Route 53 to route traffic to the CloudFront distribution.

C. Create an Amazon CloudFront distribution that has the S3 bucket as an origin. Create an AWS Global Accelerator standard accelerator that has the ALB and the CloudFront distribution as endpoints. Create a custom domain name that points to the accelerator DNS name. Use the custom domain name as an endpoint for the web application.

D. Create an Amazon CloudFront distribution that has the ALB as an origin. Create an AWS Global Accelerator standard accelerator that has the S3 bucket as an endpoint. Create two domain names. Point one domain name to the CloudFront DNS name for dynamic content. Point the other domain name to the accelerator DNS name for static content. Use the domain names as endpoints for the web application.

==========================================>

**Question**

A company uses a popular content management system (CMS) for its corporate website. However, the required patching and maintenance are burdensome. The company is redesigning its website and wants anew solution. The website will be updated four times a year and does not need to have any dynamic content available. The solution must provide high scalability and enhanced security.
Which combination of changes will meet these requirements with the LEAST operational overhead? (Choose two.)

**A. Configure Amazon CloudFront in front of the website to use HTTPS functionality.**

B. Deploy an AWS WAF web ACL in front of the website to provide HTTPS functionality.

C. Create and deploy an AWS Lambda function to manage and serve the website content.

**D. Create the new website and an Amazon S3 bucket. Deploy the website on the S3 bucket with static website hosting enabled.**

E. Create the new website. Deploy the website by using an Auto Scaling group of Amazon EC2 instances behind an Application Load Balancer.

==========================================>

**Question**

A company runs a web-based portal that provides users with global breaking news, local alerts, and weather updates. The portal delivers each user a personalized view by using mixture of static and dynamic content. Content is served over HTTPS through an API server running on an Amazon EC2 instance behind an Application Load Balancer (ALB). The company wants the portal to provide this content to its users across the world as quickly as possible.
How should a solutions architect design the application to ensure the LEAST amount of latency for all users?

**A. Deploy the application stack in a single AWS Region. Use Amazon CloudFront to serve all static and dynamic content by specifying the ALB as an origin.**

B. Deploy the application stack in two AWS Regions. Use an Amazon Route 53 latency routing policy to serve all content from the ALB in the closest Region.

C. Deploy the application stack in a single AWS Region. Use Amazon CloudFront to serve the static content. Serve the dynamic content directly from the ALB.

D. Deploy the application stack in two AWS Regions. Use an Amazon Route 53 geolocation routing policy to serve all content from the ALB in the closest Region.

==========================================>

**Question**

An online customer portal is hosted in an Amazon ECS cluster behind an Application Load Balancer. The portal is set as the origin of a CloudFront Web distribution to deliver the dynamic and static content to users in low-latency. A Cloud Engineer was assigned to configure CloudFront to communicate with your origin using HTTP or HTTPS, based on the protocol of the viewer request.

What should the Engineer implement to complete this task?

**A. Set the Origin Protocol policy of the CloudFront distribution to Match Viewer.**

B. Set the Origin Protocol policy of the CloudFront distribution to HTTP and HTTPS.

C. Set the Viewer Protocol policy of the CloudFront distribution to HTTP and HTTPS.

D. Set the Viewer Protocol policy of the CloudFront distribution to Match Viewer.