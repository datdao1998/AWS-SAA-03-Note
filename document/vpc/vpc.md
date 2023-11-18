# What is Amazon VPC?
With Amazon Virtual Private Cloud (Amazon VPC), you can launch AWS resources in a logically isolated virtual network that you've defined.

# Connect to VPC

## NAT device

### 1. NAT Gateway
* If you use a private NAT gateway to connect to a transit gateway or virtual private gateway, traffic to the destination will come from the private IP address of the private NAT gateway.
* If you use a public NAT gateway to connect to a transit gateway or virtual private gateway, traffic to the destination will come from the private IP address of the public NAT gateway unless you use an internet gateway. The public NAT gateway will only use its EIP as the source IP address when used in conjunction with an internet gateway.

### 2. NAT instances
A NAT instance provides network address translation (NAT). You can use a NAT instance to allow resources in a private subnet to communicate with destinations outside the virtual private cloud (VPC), such as the internet or an on-premises network

### 3. Comparison between NAT Gateway vs NAT instances

|  Attribute | NAT Gateway   | NAT instances   |
|---|---|---|
| Maintenance  |  Managed by AWS | Managed by you  |
|  Port forwarding | Not supported  | Manually customize the configuration to support port forwarding  |
|  Bastion servers | Not supported  |  Use as a bastion server |