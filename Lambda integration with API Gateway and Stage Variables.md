## Problem

A developer has defined a Lambda integration in Amazon API Gateway using a stage variable. However, when the developer invokes the API method, it consistently returns an "Internal server error" and a 500 status code.

## Solution

**If you create a stage variable to call a Lambda function through your API, you must add the required permissions. Update your Lambda function's resource-based AWS Identity and Access Management (IAM) policy so that it grants invoke permission to the API Gateway**
-------------------------------------------------------------------------------
If your Lambda function's resource-based policy doesn't include permissions for your API to invoke the function, API Gateway returns an Internal server error message.

If you create a stage variable to call a function through your API, you must add the required permissions by doing one of the following:

Update your Lambda function's resource-based AWS Identity and Access Management (IAM) policy so that it grants invoke permission to API Gateway.

OR

Create an IAM role that API Gateway can assume to invoke your Lambda function.

If you build an API Gateway API with standard Lambda integration using the API Gateway console, the console adds the required permissions automatically.

Example resource-based policy that grants invoke permission to API Gateway: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt5-q48-i1.jpg)
