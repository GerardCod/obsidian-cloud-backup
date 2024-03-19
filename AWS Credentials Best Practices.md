#Development #SDK 

• Overall, NEVER EVER STORE AWS CREDENTIALS IN YOUR CODE 
• Best practice is for credentials to be inherited from the credentials chain
• If using working within AWS, use IAM Roles 
	• => EC2 Instances Roles for EC2 Instances
	• => ECS Roles for ECS tasks  
	• => Lambda Roles for Lambda functions
• If working outside of AWS, use environment variables / named profiles