#Security #EC2 

## Problem

An e-commerce company has a fleet of EC2 based web servers running into very high CPU utilization issues. The development team has determined that serving secure traffic via HTTPS is a major contributor to the high CPU load.

Which of the following steps can take the high CPU load off the web servers?

## Solution

"Configure an SSL/TLS certificate on an Application Load Balancer via AWS Certificate Manager (ACM)"

"Create an HTTPS listener on the Application Load Balancer with SSL termination"

An Application load balancer distributes incoming application traffic across multiple targets, such as EC2 instances, in multiple Availability Zones. A listener checks for connection requests from clients, using the protocol and port that you configure. The rules that you define for a listener determine how the load balancer routes requests to its registered targets. Each rule consists of a priority, one or more actions, and one or more conditions.

![](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/images/component_architecture.png) via - [https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html)

To use an HTTPS listener, you must deploy at least one SSL/TLS server certificate on your load balancer. You can create an HTTPS listener, which uses encrypted connections (also known as SSL offload). This feature enables traffic encryption between your load balancer and the clients that initiate SSL or TLS sessions. As the EC2 instances are under heavy CPU load, the load balancer will use the server certificate to terminate the front-end connection and then decrypt requests from clients before sending them to the EC2 instances.

Please review this resource to understand how to associate an ACM SSL/TLS certificate with an Application Load Balancer: [https://aws.amazon.com/premiumsupport/knowledge-center/associate-acm-certificate-alb-nlb/](https://aws.amazon.com/premiumsupport/knowledge-center/associate-acm-certificate-alb-nlb/)