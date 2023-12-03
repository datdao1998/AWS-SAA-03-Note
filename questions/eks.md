**Question**

A company needs to accelerate the performance of its AI-powered medical diagnostic application by running its machine learning workloads on the edge of telecommunication carriers’ 5G networks. The application must be deployed to a Kubernetes cluster and have role-based access control (RBAC) access to IAM users and roles for cluster authentication.

Which of the following should the Solutions Architect implement to ensure single-digit millisecond latency for the application?

**A. Launch the application to an Amazon Elastic Kubernetes Service (Amazon EKS) cluster. Create node groups in Wavelength Zones for the Amazon EKS cluster via the AWS Wavelength service. Apply the AWS authenticator configuration map (aws-auth ConfigMap) to your cluster.**

B. Host the application to an Amazon Elastic Kubernetes Service (Amazon EKS) cluster. Set up node groups in AWS Wavelength Zones for the Amazon EKS cluster. Attach the Amazon EKS connector agent role (AmazonECSConnectorAgentRole) to your cluster and use AWS Control Tower for RBAC access.

C. Host the application to an Amazon EKS cluster and run the Kubernetes pods on AWS Fargate. Create node groups in AWS Wavelength Zones for the Amazon EKS cluster. Add the EKS pod execution IAM role (AmazonEKSFargatePodExecutionRole) to your cluster and ensure that the Fargate profile has the same IAM role as your Amazon EC2 node groups.

D. Launch the application to an Amazon Elastic Kubernetes Service (Amazon EKS) cluster. Create VPC endpoints for the AWS Wavelength Zones and apply them to the Amazon EKS cluster. Install the AWS IAM Authenticator for Kubernetes (aws-iam-authenticator) to your cluster.

=====================================================>

**Question**

A company wants to run applications in containers in the AWS Cloud. These applications are stateless and can tolerate disruptions within the underlying infrastructure. The company needs a solution that minimizes cost and operational overhead.
What should a solutions architect do to meet these requirements?

A. Use Spot Instances in an Amazon EC2 Auto Scaling group to run the application containers.

**B. Use Spot Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.**

C. Use On-Demand Instances in an Amazon EC2 Auto Scaling group to run the application containers.

D. Use On-Demand Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.