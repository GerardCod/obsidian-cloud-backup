#Deployment #ALB #Lambda 

## Problem

The development team at an IT company has configured an Application Load Balancer (ALB) with a Lambda function A as the target but the Lambda function A is not able to process any request from the ALB. Upon investigation, the team finds that there is another Lambda function B in the AWS account that is exceeding the concurrency limits.

How can the development team address this issue?

## Solution

**Set up reserved concurrency for the Lambda function B so that it throttles if it goes above a certain concurrency limit**

Concurrency is the number of requests that a Lambda function is serving at any given time. If a Lambda function is invoked again while a request is still being processed, another instance is allocated, which increases the function's concurrency.

To ensure that a function can always reach a certain level of concurrency, you can configure the function with reserved concurrency. When a function has reserved concurrency, no other function can use that concurrency. More importantly, reserved concurrency also limits the maximum concurrency for the function, and applies to the function as a whole, including versions and aliases.

Please review this note to understand how reserved concurrency works:

![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt1-q6-i1.jpg) via - [https://docs.aws.amazon.com/lambda/latest/dg/configuration-concurrency.html#configuration-concurrency-reserved](https://docs.aws.amazon.com/lambda/latest/dg/configuration-concurrency.html#configuration-concurrency-reserved)

Therefore using reserved concurrency for Lambda function B would limit its maximum concurrency and allow Lambda function A to execute without getting throttled.

