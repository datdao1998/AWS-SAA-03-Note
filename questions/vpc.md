**Question**

A media company has two VPCs: VPC-1 and VPC-2 with peering connection between each other. VPC-1 only contains private subnets while VPC-2 only contains public subnets. The company uses a single AWS Direct Connect connection and a virtual interface to connect their on-premises network with VPC-1.

Which of the following options increase the fault tolerance of the connection to VPC-1? (Select TWO.)

A. Establish a new AWS Direct Connect connection and private virtual interface in the same region as VPC-2.

**B. Establish a hardware VPN over the Internet between VPC-1 and the on-premises network.**

**C. Establish another AWS Direct Connect connection and private virtual interface in the same AWS region as VPC-1.**

D. Use the AWS VPN CloudHub to create a new AWS Direct Connect connection and private virtual interface in the same region as VPC-2.

E. Establish a hardware VPN over the Internet between VPC-2 and the on-premises network.

==============================>

**Question**

A large financial firm needs to set up a Linux bastion host to allow access to the Amazon EC2 instances running in their VPC. For security purposes, only the clients connecting from the corporate external public IP address 175.45.116.100 should have SSH access to the host.

Which is the best option that can meet the customer’s requirement?

A. Network ACL Inbound Rule: Protocol – UDP, Port Range – 22, Source 175.45.116.100/32

B. Network ACL Inbound Rule: Protocol – TCP, Port Range-22, Source 175.45.116.100/0

**C. Security Group Inbound Rule: Protocol – TCP. Port Range – 22, Source 175.45.116.100/32**

D. Security Group Inbound Rule: Protocol – UDP, Port Range – 22, Source 175.45.116.100/32

**Explained**

A bastion host is a special purpose computer on a network specifically designed and configured to withstand attacks. The computer generally hosts a single application, for example, a proxy server, and all other services are removed or limited to reduce the threat to the computer.

When setting up a bastion host in AWS, you should only allow the individual IP of the client and not the entire network. Therefore, in the Source,  the proper CIDR notation should be used. The /32 denotes one IP address, and the /0 refers to the entire network.

==============================>

**Question**

A company is using Amazon VPC that has a CIDR block of 10.31.0.0/27 that is connected to the on-premises data center. There was a requirement to create a Lambda function that will process massive amounts of cryptocurrency transactions every minute and then store the results to EFS. After setting up the serverless architecture and connecting the Lambda function to the VPC, the Solutions Architect noticed an increase in invocation errors with EC2 error types such as EC2ThrottledException at certain times of the day.

Which of the following are the possible causes of this issue? (Select TWO.)

**A. Your VPC does not have sufficient subnet ENIs or subnet IPs.**

B. The associated security group of your function does not allow outbound connections.

**C. You only specified one subnet in your Lambda function configuration. That single subnet runs out of available IP addresses and there is no other subnet or Availability Zone which can handle the peak load.**

D. The attached IAM execution role of your function does not have the necessary permissions to access the resources of your VPC.

E. Your VPC does not have a NAT gateway.

==============================>

**Question**

A company has a three-tier web application that is deployed on AWS. The web servers are deployed in a public subnet in a VPC. The application servers and database servers are deployed in private subnets in the same VPC. The company has deployed a third-party virtual firewall appliance from AWS Marketplace in an inspection VPC. The appliance is configured with an IP interface that can accept IP packets.
A solutions architect needs to integrate the web application with the appliance to inspect all traffic to the application before the traffic reaches the web server.
Which solution will meet these requirements with the LEAST operational overhead?

A. Create a Network Load Balancer in the public subnet of the application's VPC to route the traffic to the appliance for packet inspection.

B. Create an Application Load Balancer in the public subnet of the application's VPC to route the traffic to the appliance for packet inspection.

C. Deploy a transit gateway in the inspection VPConfigure route tables to route the incoming packets through the transit gateway.

**D. Deploy a Gateway Load Balancer in the inspection VPC. Create a Gateway Load Balancer endpoint to receive the incoming packets and forward the packets to the appliance.**

==============================>

**Question**

A company wants to migrate its on-premises data center to AWS. According to the company's compliance requirements, the company can use only the ap-northeast-3 Region. Company administrators are not permitted to connect VPCs to the internet.
Which solutions will meet these requirements? (Choose two.)

**A. Use AWS Control Tower to implement data residency guardrails to deny internet access and deny access to all AWS Regions except ap-northeast-3.**

B. Use rules in AWS WAF to prevent internet access. Deny access to all AWS Regions except ap-northeast-3 in the AWS account settings.

**C. Use AWS Organizations to configure service control policies (SCPS) that prevent VPCs from gaining internet access. Deny access to all AWS Regions except ap-northeast-3.**

D. Create an outbound rule for the network ACL in each VPC to deny all traffic from 0.0.0.0/0. Create an IAM policy for each user to prevent the use of any AWS Region other than ap-northeast-3.

E. Use AWS Config to activate managed rules to detect and alert for internet gateways and to detect and alert for new resources deployed outside of ap-northeast-3.