#Security #Cognito #CloudFront #ALB 

## Problem

A photo-sharing application manages its EC2 server fleet running behind an Application Load Balancer and the traffic is fronted by a CloudFront distribution. The development team wants to decouple the user authentication process for the application so that the application servers can just focus on the business logic.

As a Developer Associate, which of the following solutions would you recommend to address this use-case with minimal development effort?

## Solution

**Use Cognito Authentication via Cognito User Pools for your Application Load Balancer**

Application Load Balancer can be used to securely authenticate users for accessing your applications. This enables you to offload the work of authenticating users to your load balancer so that your applications can focus on their business logic. You can use Cognito User Pools to authenticate users through well-known social IdPs, such as Amazon, Facebook, or Google, through the user pools supported by Amazon Cognito or through corporate identities, using SAML, LDAP, or Microsoft AD, through the user pools supported by Amazon Cognito. You configure user authentication by creating an authenticate action for one or more listener rules. The authenticate-cognito and authenticate-oidc action types are supported only with HTTPS listeners.

![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt1-q4-i1.jpg) via - [https://docs.aws.amazon.com/elasticloadbalancing/latest/application/listener-authenticate-users.html](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/listener-authenticate-users.html)

Please make sure that you adhere to the following configurations while using CloudFront distribution in front of your Application Load Balancer: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt1-q4-i2.jpg) via - [https://docs.aws.amazon.com/elasticloadbalancing/latest/application/listener-authenticate-users.html](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/listener-authenticate-users.html)

Exam Alert:

Please review the following note to understand the differences between Cognito User Pools and Cognito Identity Pools: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt1-q4-i3.jpg) via - [https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html](https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html)