#Troubleshooting_and_Optimization  #S3 

## Problem

A development team has been using Amazon S3 service as an object store. With Amazon S3 turning strongly consistent, the team wants to understand the impact of this change on its data storage practices.

As a developer associate, can you identify the key characteristics of the strongly consistent data model followed by S3?

## Solution

**If you delete a bucket and immediately list all buckets, the deleted bucket might still appear in the list** - Bucket configurations have an eventual consistency model. If you delete a bucket and immediately list all buckets, the deleted bucket might still appear in the list.

**A process deletes an existing object and immediately tries to read it. Amazon S3 will not return any data as the object has been deleted** - Amazon S3 provides strong read-after-write consistency for PUTs and DELETEs of objects in your Amazon S3 bucket in all AWS Regions. This applies to both writes to new objects as well as PUTs that overwrite existing objects and DELETEs.

Amazon S3 data consistency model: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt6-q44-i1.jpg) via - [https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html#ConsistencyModel](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html#ConsistencyModel)