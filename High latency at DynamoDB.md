#Troubleshooting_and_Optimization #DynamoDB 

## Problem

An organization with high data volume workloads have successfully moved to DynamoDB after having many issues with traditional database systems. However, a few months into production, DynamoDB tables are consistently recording high latency.

As a Developer Associate, which of the following would you suggest to reduce the latency?

## Solution

Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup, and restore and in-memory caching for internet-scale applications.

**Consider using Global tables if your application is accessed by globally distributed users** - If you have globally dispersed users, consider using global tables. With global tables, you can specify the AWS Regions where you want the table to be available. This can significantly reduce latency for your users. So, reducing the distance between the client and the DynamoDB endpoint is an important performance fix to be considered.

**Use eventually consistent reads in place of strongly consistent reads whenever possible** - If your application doesn't require strongly consistent reads, consider using eventually consistent reads. Eventually consistent reads are cheaper and are less likely to experience high latency.