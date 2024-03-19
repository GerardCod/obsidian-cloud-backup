#Deployment #ElasticBeanstalk 

## Problem

A retail company manages its IT infrastructure on AWS Cloud via Elastic Beanstalk. The development team at the company is planning to deploy the next version with MINIMUM application downtime and the ability to rollback quickly in case deployment goes wrong.

As a Developer Associate, which of the following options would you recommend to the development team?

## Solution

**Deploy the new version to a separate environment via Blue/Green Deployment, and then swap Route 53 records of the two environments to redirect traffic to the new version**

With deployment policies such as 'All at once', AWS Elastic Beanstalk performs an in-place update when you update your application versions and your application can become unavailable to users for a short period of time. You can avoid this downtime by performing a blue/green deployment, where you deploy the new version to a separate environment, and then swap CNAMEs (via Route 53) of the two environments to redirect traffic to the new version instantly. In case of any deployment issues, the rollback process is very quick via swapping the URLs for the two environments.

Overview of Elastic Beanstalk Deployment Policies: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt1-q10-i1.jpg) via - [https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.deploy-existing-version.html](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.deploy-existing-version.html)