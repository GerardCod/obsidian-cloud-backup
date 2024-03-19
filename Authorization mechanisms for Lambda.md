#Security #Lambda #API_Gateway

You've just deployed an AWS Lambda function. The lambda function will be invoked via the API Gateway. The API Gateway will need to control access to it.

What are the mechanisms supported by API Gateway?

- IAM permissions with v4: They can be applied to an entire API or individual methods.
- Cognito User Pools: Use Cognito User Pools to create customizable authentication and authorization solutions for your REST APIs.
- Lambda Authorizer: Control access to REST API methods using bearer token authentication as well as information described by headers, paths, query strings, stage variables, or context variables request parameter.