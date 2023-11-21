### Q1. The systems administrator at a company wants to set up a highly available architecture for a bastion host solution. As a solutions architect, which of the following options would you recommend as the solution?

**Answer** : Create a public Network Load Balancer that links to EC2 instances that are bastion hosts managed by an ASG

**Explained** : Bastion Hosts are using the SSH protocol, which is a TCP based protocol on port 22. They must be publicly accessible.

-> Here, the correct answer is to use a Network Load Balancer, which supports TCP traffic, and will automatically allow you to connect to the EC2 instance in the backend.