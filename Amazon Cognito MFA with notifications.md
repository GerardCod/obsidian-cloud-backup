#Development #Cognito #Lambda 

Regarding the next scenario: A business-critical mobile application uses Amazon Cognito user pools with multi-factor authentication (MFA) enabled for all its users. The application manages confidential data about the company's sales forecasts and product launches. Considering the highly critical nature of the application, the company wants to track every user login activity via a notification sent as an email to the security team.

What would be recommended as the MOST optimal way of implementing this requirement within a short period?

**Create an AWS Lambda function that uses Amazon Simple Email Service to send an email notification to the concerned security team. Configure this function as Amazon Cognito post-authentication Lambda trigger**
-------------------------------------------------------------------------------
Amazon Cognito invokes Post authentication Lambda trigger after signing in a user, you can add custom logic after Amazon Cognito authenticates the user.

Post-authentication Lambda flows: 
![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt5-q37-i1.jpg)
