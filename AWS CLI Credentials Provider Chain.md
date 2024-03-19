#Development #CLI 

• The CLI will look for credentials in this order:
1. Command line options – --region, --output, and --profile
2. Environmentvariables AWS_ACCESS_KEY_ID,AWS_SECRET_ACCESS_KEY, and AWS_SESSION_TOKEN
3. CLI credentials file –aws configure  ~/.aws/credentials on Linux / Mac & C:\Users\user\.aws\credentials on Windows
4. CLI configuration file – aws configure  ~/.aws/config on Linux / macOS & C:\Users\USERNAME\.aws\config on Windows
5. Container credentials – for ECS tasks  
6. Instance profile credentials – for EC2 Instance Profiles