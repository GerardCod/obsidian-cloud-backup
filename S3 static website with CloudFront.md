#Troubleshooting_and_Optimization #CloudFront #S3 

## Problem

A media application uses Amazon CloudFront distribution to distribute static content configured on an Amazon S3 bucket. The application is used across different countries and various AWS Regions. Some regions have been experiencing latency when there is a cache miss on CloudFront.

Which of the following configuration changes will you suggest to decrease latency and improve user performance?

## Solution

**Redirect requests on cache misses to the Amazon S3 bucket nearest to the user country. Create a CloudFront function to redirect requests based on the value of the CloudFront-Viewer-Country header. Associate the CloudFront function with the distribution's viewer request event**

With CloudFront Functions in Amazon CloudFront, you can write lightweight functions in JavaScript for high-scale, latency-sensitive CDN customizations. Your functions can manipulate the requests and responses that flow through CloudFront, perform basic authentication and authorization, generate HTTP responses at the edge, and more.

When you associate a CloudFront function with a CloudFront distribution, CloudFront intercepts requests and responses at CloudFront edge locations and passes them to your function. You can invoke CloudFront functions when the following events occur: 1. When CloudFront receives a request from a viewer (viewer request): The function executes when CloudFront receives a request from a viewer before it checks to see whether the requested object is in the CloudFront cache.

1. Before CloudFront returns the response to the viewer (viewer response): The function executes before returning the requested file to the viewer. Note that the function executes regardless of whether the file is already in the CloudFront cache.

We use the value of the CloudFront-Viewer-Country header to update the S3 bucket domain name to a bucket in a Region that is closer to the viewer. This can be useful in several ways: 1. It reduces latencies when the Region specified is nearer to the viewer's country. 2. It provides data sovereignty by making sure that data is served from an origin that's in the same country that the request came from.

The example below shows how a Lambda handler is used to change response based on user country. A similar CloudFront function can be defined to direct user traffic to the nearest S3 bucket.

Example for redirecting viewer requests to a country-specific URL: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt6-q32-i1.jpg) via - [https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/lambda-examples.html#lambda-examples-content-based-S3-origin-request-trigger](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/lambda-examples.html#lambda-examples-content-based-S3-origin-request-trigger)
Choosing between CloudFront Functions and Lambda@Edge: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt6-q32-i2.jpg) via - [https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/edge-functions.html](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/edge-functions.html)