A large corporation has several Windows file servers in various departments within its on-premises data center. To improve its data management and scalability, the corporation has to migrate and integrate its files into an Amazon FSx for Windows File Server file system while keeping the current file permissions intact.

Which of the following solutions will fulfill the company’s requirements? (Select TWO.)

**A. Acquire an AWS Snowcone device, then connect with the on-premises network. Use AWS OpsHub to launch the AWS DataSync agent AMI and activate the agent via the AWS Management Console. Schedule DataSync tasks to transfer the data to the Amazon FSx for Windows File Server file system.**

**B. Set up AWS DataSync agents on the corporation's on-premises file servers and schedule DataSync tasks for transferring data to the Amazon FSx for Windows File Server file system.**

C. Order an AWS Snowball Edge Storage Optimized device, link it to the on-premises network, and transfer data using the AWS CLI. Return the device to AWS for data import into Amazon S3. Configure AWS DataSync tasks to migrate the data from S3 to the Amazon FSx for Windows File Server file system

D. Utilize the AWS CLI to copy the file shares from each on-premises file server to an Amazon S3 bucket. Then, schedule AWS DataSync tasks to move the data from S3 to the Amazon FSx for Windows File Server file system

E. Extract the drives from the individual file servers and transport them to AWS via the AWS Snowmobile service. Import the file server data into Amazon S3 from Snowmobile. Afterward, configure the AWS DataSync tasks to sync the data from S3 to the Amazon FSx for Windows File Server file system.