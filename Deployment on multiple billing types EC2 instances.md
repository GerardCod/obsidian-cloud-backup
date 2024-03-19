#Development #EC2 #ASG #CodeDeploy 

## Problem

A developer is configuring an Amazon EC2 Auto Scaling Group that has to launch both Spot and On-Demand instances based on the requirement. Also, the CodeDeploy agent has to be automatically installed on these EC2 instances. All the EC2 instances are running on the Amazon Linux operating system.

What is the most operationally efficient way to configure this requirement?

## Solution

**Use launch templates to configure the EC2 Auto Scaling Group for On-Demand and spot instances. When you create a launch template use the User data field to add a configuration script that runs when the instance starts. This shell script can, in turn, install the CodeDeploy agent**

A launch template specifies instance configuration information that includes the ID of the Amazon Machine Image (AMI), the instance type, a key pair, security groups, and other parameters used to launch EC2 instances. Defining a launch template instead of a launch configuration allows you to have multiple versions of a launch template.

When you create a launch template, you can use the User data field to add a configuration script that runs when the instance starts. This shell script installs the CodeDeploy agent for all AWS Regions and supported Amazon Linux and Ubuntu distributions. You can configure CodeDeploy to auto-update on boot by setting the AUTOUPDATE variable to true.