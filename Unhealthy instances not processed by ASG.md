#Troubleshooting_and_Optimization #ElasticBeanstalk 

## Problem

A startup manages its Cloud resources with Elastic Beanstalk. The environment consists of few Amazon EC2 instances, an Auto Scaling Group (ASG), and an Elastic Load Balancer. Even after the Load Balancer marked an EC2 instance as unhealthy, the ASG has not replaced it with a healthy instance.

As a Developer, suggest the necessary configurations to automate the replacement of unhealthy instance.

## Solution

**The health check type of your instance's Auto Scaling group, must be changed from EC2 to ELB by using a configuration file** - By default, the health check configuration of your Auto Scaling group is set as an EC2 type that performs a status check of EC2 instances. To automate the replacement of unhealthy EC2 instances, you must change the health check type of your instance's Auto Scaling group from EC2 to ELB by using a configuration file.