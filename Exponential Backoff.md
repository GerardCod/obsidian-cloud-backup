#Development #SDK 

• If you get ThrottlingException intermittently, use exponential backoff
• Retry mechanism already included in AWS SDK API calls
• Must implement yourself if using the AWS API as-is or in specific cases 
• Must only implement the retries on 5xx server errors and throttling  
• Do not implement on the 4xx client errors