#Development #SDK 

• The Java SDK (example) will look for credentials in this order
1. Java system properties – aws.accessKeyId and aws.secretKey
2. Environment variables –  AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY
3. The default credential profiles file – ex at: ~/.aws/credentials, shared by many SDK
4. Amazon ECS container credentials – for ECS containers
5. Instance profile credentials– used on EC2 instances