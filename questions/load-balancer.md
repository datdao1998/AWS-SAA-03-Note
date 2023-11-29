**Question** 

A company has a website hosted on AWS. The website is behind an Application Load Balancer (ALB) that is configured to handle HTTP and HTTPS separately. The company wants to forward all requests to the website so that the requests will use HTTPS.
What should a solutions architect do to meet this requirement?

A. Update the ALB’s network ACL to accept only HTTPS traffic.

B. Create a rule that replaces the HTTP in the URL with HTTPS.

**C. Create a listener rule on the ALB to redirect HTTP traffic to HTTPS.**

D. Replace the ALB with a Network Load Balancer configured to use Server Name Indication (SNI).

=====================================================>

**Question**

A startup uses a fleet of Amazon EC2 servers to manage its CRM application. These Amazon EC2 servers are behind Elastic Load Balancing (ELB). Which of the following configurations are NOT allowed for Elastic Load Balancing?

**A. Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. Two of these instances are deployed in Availability Zone A of us-east-1 region and the other two instances are deployed in Availability Zone B of us-west-1 region**

B. Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed across two Availability Zones of us-east-1 region

C. Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed in Availability Zone A of us-east-1 region

D. Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed in Availability Zone B of us-west-1 region

**Explained**

Elastic Load Balancer automatically distributes incoming traffic across multiple targets – Amazon EC2 instances, containers, IP addresses, and Lambda functions – in multiple Availability Zones and ensures only healthy targets receive traffic. ELB cannot distribute incoming traffic for targets deployed in different regions. 

=====================================================>

**Question**

A company has implemented a self-managed DNS solution on three Amazon EC2 instances behind a Network Load Balancer (NLB) in the us-west-2 Region. Most of the company's users are located in the United States and Europe. The company wants to improve the performance and availability of the solution. The company launches and configures three EC2 instances in the eu-west-1 Region and adds the EC2 instances as targets for a new NLB.
Which solution can the company use to route traffic to all the EC2 instances?

A. Create an Amazon Route 53 geolocation routing policy to route requests to one of the two NLBs. Create an Amazon CloudFront distribution. Use the Route 53 record as the distribution’s origin.

**B. Create a standard accelerator in AWS Global Accelerator. Create endpoint groups in us-west-2 and eu-west-1. Add the two NLBs as endpoints for the endpoint groups.**

C. Attach Elastic IP addresses to the six EC2 instances. Create an Amazon Route 53 geolocation routing policy to route requests to one of the six EC2 instances. Create an Amazon CloudFront distribution. Use the Route 53 record as the distribution's origin.

D. Replace the two NLBs with two Application Load Balancers (ALBs). Create an Amazon Route 53 latency routing policy to route requests to one of the two ALBs. Create an Amazon CloudFront distribution. Use the Route 53 record as the distribution’s origin.

=====================================================>

**Question**

A company's HTTP application is behind a Network Load Balancer (NLB). The NLB's target group is configured to use an Amazon EC2 Auto Scaling group with multiple EC2 instances that run the web service.
The company notices that the NLB is not detecting HTTP errors for the application. These errors require a manual restart of the EC2 instances that run the web service. The company needs to improve the application's availability without writing custom scripts or code.
What should a solutions architect do to meet these requirements?

A. Enable HTTP health checks on the NLB, supplying the URL of the company's application.

B. Add a cron job to the EC2 instances to check the local application's logs once each minute. If HTTP errors are detected, the application will restart.

**C. Replace the NLB with an Application Load Balancer. Enable HTTP health checks by supplying the URL of the company's application. Configure an Auto Scaling action to replace unhealthy instances.**

D. Create an Amazon CloudWatch alarm that monitors the UnhealthyHostCount metric for the NLB. Configure an Auto Scaling action to replace unhealthy instances when the alarm is in the ALARM state.