#Security #KMS 

## Problem

An e-commerce application posts its order transactions in bulk to an accounting application for further processing. Due to changes in the compliance rules, all the transactions are being encrypted with AWS Key Management Service (AWS KMS) key before posting to the accounting application. Post this change, the testers have raised tickets regarding the application receiving a ThrottlingException error.

What measures should a developer take to fix this issue MOST optimally?

## Solution

**Reduce the rate of requests and consider using the backoff and retry logic**

Each AWS SDK implements automatic retry logic. The AWS SDK for Java automatically retries requests, and you can configure the retry settings. In addition to simple retries, each AWS SDK implements an exponential backoff algorithm for better flow control. The idea behind exponential backoff is to use progressively longer waits between retries for consecutive error responses. You should implement a maximum delay interval, as well as a maximum number of retries. The maximum delay interval and the maximum number of retries are not necessarily fixed values and should be set based on the operation being performed, as well as other local factors, such as network latency.

**Use the data key caching feature with the AWS Encryption SDK encryption library**

Data key caching stores data keys and related cryptographic material in a cache. When you encrypt or decrypt data, the AWS Encryption SDK looks for a matching data key in the cache. If it finds a match, it uses the cached data key rather than generating a new one. Data key caching can improve performance, reduce cost, and help you stay within service limits as your application scales.

Your application can benefit from data key caching if: 1. It can reuse data keys. 2. It generates numerous data keys. 3. Your cryptographic operations are unacceptably slow, expensive, limited, or resource-intensive.

Data key caching is an optional feature of the AWS Encryption SDK that you should use cautiously. By default, the AWS Encryption SDK generates a new data key for every encryption operation. This technique supports cryptographic best practices, which discourage excessive reuse of data keys. In general, use data key caching only when it is required to meet your performance goals. Then, use the data key caching security thresholds to ensure that you use the minimum amount of caching required to meet your cost and performance goals.

Best practices to troubleshoot ThrottlingException errors: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt5-q16-i1.jpg) via - [https://aws.amazon.com/premiumsupport/knowledge-center/kms-throttlingexception-error/](https://aws.amazon.com/premiumsupport/knowledge-center/kms-throttlingexception-error/)

