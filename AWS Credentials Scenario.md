#Development #Credentials 

- An application deployed on an EC2 instance is using environment variables with credentials from an IAM user to call the Amazon S3 API.
- The IAM user has S3FullAccess permissions.
- The application only uses one S3 bucket, so according to best practices: 
	-  An IAM Role & EC2 Instance Profile was created for the EC2 instance  
    - The Role was assigned the minimum permissions to access that one S3 bucket
- The IAM Instance Profile was assigned to the EC2 instance, but it still had access to all S3 buckets.Why? 
	the credentials chain is still giving priorities to the environment variables