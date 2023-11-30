* A network access control list (ACL) allows or denies specific inbound or outbound traffic at the **subnet level**.

* You can use the default network ACL for your VPC, or you can create a custom network ACL for your VPC with rules that are similar to the rules for your security groups in order to add an additional layer of security to your VPC.

* There is no additional charge for using network ACLs.

* Rules are evaluated starting with the lowest numbered rule. As soon as a rule matches traffic, it’s applied immediately regardless of any higher-numbered rule that may contradict it.