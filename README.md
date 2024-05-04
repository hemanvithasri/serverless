# serverless
sending email using SQS, Lambda and SES

Services:
The mechanism you are referring to is the flow of data between various AWS services, such as:
AWS SQS
AWS IAM
AWS Lambda
AWS SES
Mechanism:
Here is a brief explanation of how these services are used:
Amazon Simple Queue Service (SQS) is a fully managed message queuing service offered by Amazon Web Services (AWS). While SQS is primarily used for decoupling and scaling distributed systems, it can indirectly play a role in sending emails in AWS-based applications through the workflow
In the connection between Lambda and SQS, an IAM role is assigned to the Lambda function with permissions to read messages from the SQS queue. This role allows Lambda to receive messages from the queue, triggering the function to process them, facilitating asynchronous message processing.
Additionally, the Lambda function communicates with SNS, a fully managed, highly available, robust, and secure pub/sub messaging service that facilitates the decoupling and scalability of distributed systems, serverless apps, and microservices. Messages are sent to a subject via SNS and can be received by several recipients, including email addresses, mobile devices, and other endpoints.
Lastly, the Lambda function communicates with SES, an extremely flexible, scalable, and affordable email sending service that lets companies send marketing emails, transactional emails, and other kinds of excellent material to their clientele. To notify the user via email that their form submission has been received and processed, SES is employed.
