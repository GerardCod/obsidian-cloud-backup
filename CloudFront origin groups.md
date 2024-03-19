#Troubleshooting_and_Optimization #CloudFront 

## Problem

A video streaming application uses Amazon CloudFront for its data distribution. The development team has decided to use CloudFront with origin failover for high availability.

Which of the following options are correct while configuring CloudFront with Origin Groups?

## Solution

**CloudFront routes all incoming requests to the primary origin, even when a previous request failed over to the secondary origin**

CloudFront routes all incoming requests to the primary origin, even when a previous request failed over to the secondary origin. CloudFront only sends requests to the secondary origin after a request to the primary origin fails.

**CloudFront fails over to the secondary origin only when the HTTP method of the viewer request is GET, HEAD or OPTIONS**

CloudFront fails over to the secondary origin only when the HTTP method of the viewer request is GET, HEAD, or OPTIONS. CloudFront does not failover when the viewer sends a different HTTP method (for example POST, PUT, and so on).

How origin failover works: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt6-q41-i1.jpg) via - [https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html)