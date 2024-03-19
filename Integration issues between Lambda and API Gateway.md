#Development #API_Gateway #Lambda 

## Problem

A developer has just integrated an AWS Lambda function to an Amazon API Gateway API. The integration has led to errors that the developer is unable to troubleshoot. The developer has decided to enable CloudWatch logging at the method level for the API Gateway API.

What are the key points of consideration while configuring configuring method-level logging for the API Gateway?

## Solution

**AWS Security Token Service(STS) is used by API Gateway for logging data to CloudWatch logs. Hence, AWS STS has to be enabled for the Region that you're using**

API Gateway calls AWS Security Token Service to assume the IAM role, so make sure that AWS STS is enabled for the Region. If you receive an error when setting the IAM role ARN, check your AWS Security Token Service account settings to make sure that AWS STS is enabled in the Region that you're using.

**To enable CloudWatch Logs for all or only some of the methods, you must also specify the ARN of an IAM role that enables API Gateway to write information to CloudWatch Logs on behalf of your user. The IAM role must also contain the following trust relationship statement**

To enable CloudWatch Logs for all or only some of the methods, you must also specify the ARN of an IAM role that enables API Gateway to write information to CloudWatch Logs on behalf of your user. To do so, choose `Settings` from the APIs main navigation pane. Then enter the ARN of an IAM role in the `CloudWatch log role ARN` text field. The IAM role must also contain the trust relationship statement.

Policy of AmazonAPIGatewayPushToCloudWatchLogs for IAM role: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt6-q9-i1.jpg) via - [https://docs.aws.amazon.com/apigateway/latest/developerguide/stages.html#how-to-stage-settings-console](https://docs.aws.amazon.com/apigateway/latest/developerguide/stages.html#how-to-stage-settings-console)

