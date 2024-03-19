#Development #Lambda 

Regarding the next scenario:

Your Lambda function must use the Node.js drivers to connect to your RDS PostgreSQL database in your VPC.

How do you bundle your Lambda function to add the dependencies?

**Put the function and the dependencies in one folder and zip them together**
A deployment package is a ZIP archive that contains your function code and dependencies. You need to create a deployment package if you use the Lambda API to manage functions, or if you need to include libraries and dependencies other than the AWS SDK. You can upload the package directly to Lambda, or you can use an Amazon S3 bucket, and then upload it to Lambda. If the deployment package is larger than 50 MB, you must use Amazon S3. This is the standard way of packaging Lambda functions.

	Any other proposal is incorrect as there is only one way to deploy a Lambda function, which is to provide the zip file with all the dependencies that it will need.