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