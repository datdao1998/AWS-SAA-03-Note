**Question**

A social media application lets users upload photos and perform image editing operations. The application offers two classes of service: pro and lite. The product team wants the photos submitted by pro users to be processed before those submitted by lite users. Photos are uploaded to Amazon S3 and the job information is sent to Amazon SQS.
As a solutions architect, which of the following solutions would you recommend?

**A. Create two Amazon SQS standard queues: one for pro and one for lite. Set up Amazon EC2 instances to prioritize polling for the pro queue over the lite queue**

B. Create two Amazon SQS standard queues: one for pro and one for lite. Set the lite queue to use short polling and the pro queue to use long polling

C. Create two Amazon SQS FIFO queues: one for pro and one for lite. Set the lite queue to use short polling and the pro queue to use long polling

D. Create one Amazon SQS standard queue. Set the visibility timeout of the pro photos to zero. Set up Amazon EC2 instances to prioritize visibility settings so pro photos are processed first 

**Explained**

AWS recommends using separate queues to provide prioritization of work. Therefore, for the given use case, you need to create an Amazon SQS standard queue for processing pro users' photos and another Amazon SQS standard queue for processing lite users' photos. Then you can configure Amazon EC2 instances to prioritize polling for the pro queue over the lite queue.