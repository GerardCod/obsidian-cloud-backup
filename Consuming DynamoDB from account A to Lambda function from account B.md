#Development #Lambda #DynamoDB 

## Problem

The development team at a retail organization wants to allow a Lambda function in its AWS Account A to access a DynamoDB table in another AWS Account B.

As a Developer Associate, which of the following solutions would you recommend for the given use-case?

## Solution

**Create an IAM role in account B with access to DynamoDB. Modify the trust policy of the role in Account B to allow the execution role of Lambda to assume this role. Update the Lambda function code to add the AssumeRole API call**

You can give a Lambda function created in one account ("account A") permissions to assume a role from another account ("account B") to access resources such as DynamoDB or S3 bucket. You need to create an execution role in Account A that gives the Lambda function permission to do its work. Then you need to create a role in account B that the Lambda function in account A assumes to gain access to the cross-account DynamoDB table. Make sure that you modify the trust policy of the role in Account B to allow the execution role of Lambda to assume this role. Finally, update the Lambda function code to add the AssumeRole API call.

Sample use-case to configure a Lambda function to assume a role from another AWS account: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt1-q1-i1.jpg) via - [https://aws.amazon.com/premiumsupport/knowledge-center/lambda-function-assume-iam-role/](https://aws.amazon.com/premiumsupport/knowledge-center/lambda-function-assume-iam-role/)