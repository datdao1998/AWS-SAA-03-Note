**Network Load Balancer** is best suited for use-cases involving low latency and high throughput workloads that involve scaling to millions of requests per second. 

**Network Load Balancer** operates at the connection level (Layer 4), routing connections to targets - Amazon EC2 instances, microservices, and containers – within Amazon Virtual Private Cloud (Amazon VPC) based on IP protocol data.

**Network Load Balancer** functions at the fourth layer of the Open Systems Interconnection (OSI) model. It can handle millions of requests per second.

**Network Load Balancers** expose a fixed IP to the public web, therefore allowing your application to be predictably reached using these IPs, while allowing you to scale your application behind tshe Network Load Balancer using an ASG.

**Network Load Balancers** don't support security groups, based on the target group configurations, the IP addresses of the clients or the private IP addresses associated with the Network Load Balancers must be allowed on the web server's security group.