#Development #VPC 

## Problem

Your company has a load balancer in a VPC configured to be internet facing. The public DNS name assigned to the load balancer is `myDns-1234567890.us-east-1.elb.amazonaws.com`. When your client applications first load they capture the load balancer DNS name and then resolve the IP address for the load balancer so that they can directly reference the underlying IP.

It is observed that the client applications work well but unexpectedly stop working after a while. What is the reason for this?

## Solution

**The load balancer is highly available and its public IP may change. The DNS name is constant**

When your load balancer is created, it receives a public DNS name that clients can use to send requests. The DNS servers resolve the DNS name of your load balancer to the public IP addresses of the load balancer nodes for your load balancer. Never resolve the IP of a load balancer as it can change with time. You should always use the DNS name.