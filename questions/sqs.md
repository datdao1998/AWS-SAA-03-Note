**Question**

A social media application lets users upload photos and perform image editing operations. The application offers two classes of service: pro and lite. The product team wants the photos submitted by pro users to be processed before those submitted by lite users. Photos are uploaded to Amazon S3 and the job information is sent to Amazon SQS.
As a solutions architect, which of the following solutions would you recommend?

**A. Create two Amazon SQS standard queues: one for pro and one for lite. Set up Amazon EC2 instances to prioritize polling for the pro queue over the lite queue**

B. Create two Amazon SQS standard queues: one for pro and one for lite. Set the lite queue to use short polling and the pro queue to use long polling

C. Create two Amazon SQS FIFO queues: one for pro and one for lite. Set the lite queue to use short polling and the pro queue to use long polling

D. Create one Amazon SQS standard queue. Set the visibility timeout of the pro photos to zero. Set up Amazon EC2 instances to prioritize visibility settings so pro photos are processed first 

**Explained**

AWS recommends using separate queues to provide prioritization of work. Therefore, for the given use case, you need to create an Amazon SQS standard queue for processing pro users' photos and another Amazon SQS standard queue for processing lite users' photos. Then you can configure Amazon EC2 instances to prioritize polling for the pro queue over the lite queue.

=====================================================>

**Question**

A company has several microservices that send messages to an Amazon SQS queue and a backend application that poll the queue to process the messages. The company also has a Service Level Agreement (SLA) which defines the acceptable amount of time that can elapse from the point when the messages are received until a response is sent. The backend operations are I/O-intensive as the number of messages is constantly growing, causing the company to miss its SLA. The Solutions Architect must implement a new architecture that improves the application’s processing time and load management.

Which of the following is the MOST effective solution that can satisfy the given requirement?


**A. Create an AMI of the backend application’s EC2 instance. Use the image to set up an Auto Scaling group and configure a target tracking scaling policy based on the ApproximateAgeOfOldestMessage metric.**

B. Create an AMI of the backend application's EC2 instance and replace it with a larger instance size.

C. Create an AMI of the backend application’s EC2 instance. Use the image to set up an Auto Scaling group and configure a target tracking scaling policy based on the CPUUtilization metric with a target value of 80%.

D. Create an AMI of the backend application's EC2 instance and launch it to a cluster placement group.

=====================================================>

**Question**

The start-up company that you are working for has a batch job application that is currently hosted on an EC2 instance. It is set to process messages from a queue created in SQS with default settings. You configured the application to process the messages once a week. After 2 weeks, you noticed that not all messages are being processed by the application.

What is the root cause of this issue?

A. Missing permissions in SQS.

B. The SQS queue is set to short-polling.

**C. Amazon SQS has automatically deleted the messages that have been in a queue for more than the maximum message retention period.**

D. The batch job application is configured to long polling.