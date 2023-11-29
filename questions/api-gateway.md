**Question** A company has registered its domain name with Amazon Route 53. The company uses Amazon API Gateway in the ca-central-1 Region as a public interface for its backend microservice APIs. Third-party services consume the APIs securely. The company wants to design its API Gateway URL with the company’s domain name and corresponding certificate so that the third-party services can use HTTPS.
Which solution will meet these requirements?

A. Create stage variables in API Gateway with Name=”Endpoint-URL” and Value=”Company Domain Name” to overwrite the default URL. Import the public certificate associated with the company’s domain name into AWS Certificate Manager (ACM).

B. Create Route 53 DNS records with the company’s domain name. Point the alias record to the Regional API Gateway stage endpoint. Import the public certificate associated with the company’s domain name into AWS Certificate Manager (ACM) in the us-east-1 Region.

**C. Create a Regional API Gateway endpoint. Associate the API Gateway endpoint with the company’s domain name. Import the public certificate associated with the company’s domain name into AWS Certificate Manager (ACM) in the same Region. Attach the certificate to the API Gateway endpoint. Configure Route 53 to route traffic to the API Gateway endpoint.**

D. Create a Regional API Gateway endpoint. Associate the API Gateway endpoint with the company’s domain name. Import the public certificate associated with the company’s domain name into AWS Certificate Manager (ACM) in the us-east-1 Region. Attach the certificate to the API Gateway APIs. Create Route 53 DNS records with the company’s domain name. Point an A record to the company’s domain name.


=====================================>

**Question**

A bicycle sharing company is developing a multi-tier architecture to track the location of its bicycles during peak operating hours. The company wants to use these data points in its existing analytics platform A solutions architect must determine the most viable multi- tier option to support this architecture. The data points must be accessible from the REST API. Which action meets these requirements for storing and retrieving location data?

A. Use Amazon Athena with Amazon S3

**B. Use Amazon API Gateway with AWS Lambda**

C. Use Amazon QuickSight with Amazon Redshift

D. Use Amazon API Gateway with Amazon Kinesis Data Analytics

=====================================>

**Question**

An e-commerce company uses a regional Amazon API Gateway to host its public REST APIs. The API Gateway endpoint is accessed through a custom domain name configured using an Amazon Route 53 alias record. As part of its continuous improvement efforts, the company wants to release a new version of its APIs which includes enhanced features and performance optimizations.

How can the company minimize customer impact, and ensure MINIMAL data loss during the update process in the MOST cost-effective manner?

**A. Implement a canary release deployment strategy for the API Gateway. Deploy the latest version of the APIs to a canary stage and direct a portion of the user traffic to this stage. Verify the new APIs. Gradually increase the traffic percentage, monitor for any issues, and, if successful, promote the canary stage to production.**

B. Modify the existing API Gateway with the updated version of the APIs, but keep the same custom domain name for the new API Gateway by using the import-to-update operation in either overwrite or merge mode.

C. Create a new API Gateway with the updated version of the APIs in OpenAPI JSON or YAML file format, but keep the same custom domain name for the new API Gateway.

D. Implement a blue-green deployment strategy for the API Gateway. Deploy the latest version of the APIs to the green environment and direct some of the user traffic to it. Verify the new APIs. If it is thoroughly verified, deploy the green environment to production.