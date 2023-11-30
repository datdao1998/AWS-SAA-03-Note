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