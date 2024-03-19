#Development #KMS 

## Problem

A developer at a university is encrypting a large XML payload transferred over the network using AWS KMS and wants to test the application before going to production.

What is the maximum data size supported by AWS KMS?

## Solution

**4 KB**

You can encrypt up to 4 kilobytes (4096 bytes) of arbitrary data such as an RSA key, a database password, or other sensitive information.

While AWS KMS does support sending data up to 4 KB to be encrypted directly, envelope encryption can offer significant performance benefits. When you encrypt data directly with AWS KMS it must be transferred over the network. Envelope encryption reduces the network load since only the request and delivery of the much smaller data key go over the network. The data key is used locally in your application or encrypting AWS service, avoiding the need to send the entire block of data to AWS KMS and suffer network latency.