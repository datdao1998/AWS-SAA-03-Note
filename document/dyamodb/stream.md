1. Amazon DynamoDB stream is an ordered flow of information about changes to items in Amazon DynamoDB table. When you enable a stream on a table, DynamoDB captures information about every modification to data items in the table. 

    Whenever an application creates, updates, or deletes items in the table, DynamoDB Streams writes a stream record with the primary key attributes of the items that were modified. A stream record contains information about a data modification to a single item in a DynamoDB table.
2. Amazon DynamoDB Streams will contain a stream of all the changes that happen to an Amazon DynamoDB table. It can be chained with an AWS Lambda function that will be triggered to react to these changes, one of which is the developer's milestone.