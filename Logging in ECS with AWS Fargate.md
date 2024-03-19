#Development #ECS #Fargate

## Problem

An application runs on Amazon Elastic Container Service (Amazon ECS) on AWS Fargate. The company's audit requirements mandate that logging and storing of application log data must be done centrally on AWS.

How will you configure this requirement?

## Solution

**Use the awslogs log driver to configure the containers in your tasks to send log information to CloudWatch Logs. Add the required `logConfiguration` parameters to your task definition**

Using the awslogs log driver you can configure the containers in your tasks to send log information to CloudWatch Logs. If you're using the Fargate launch type for your tasks, you need to add the required logConfiguration parameters to your task definition to turn on the awslogs log driver.

Before your containers can send logs to CloudWatch, you must specify the awslogs log driver for containers in your task definition. The example task definition JSON that follows has a logConfiguration object specified for each container. One is for the WordPress container that sends logs to a log group called awslogs-wordpress. The other is for a MySQL container that sends logs to a log group that's called awslogs-mysql. Both containers use the awslogs-example log stream. prefix.

Specifying a log configuration in your task definition: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt6-q26-i2.jpg) via - [https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_awslogs.html#specify-log-config](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_awslogs.html#specify-log-config)

