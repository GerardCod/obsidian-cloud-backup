#Deployment #ECR 

## Problem

You are working for a technology startup building web and mobile applications. You would like to pull Docker images from the ECR repository called `demo` so you can start running local tests against the latest application version.

## Solution

Correct options:

**`$(aws ecr get-login --no-include-email)`**
**`docker pull 1234567890.dkr.ecr.eu-west-1.amazonaws.com/demo:latest`**

The get-login command retrieves a token that is valid for a specified registry for 12 hours, and then it prints a docker login command with that authorization token. You can execute the printed command to log in to your registry with Docker, or just run it automatically using the $() command wrapper. After you have logged in to an Amazon ECR registry with this command, you can use the Docker CLI to push and pull images from that registry until the token expires. The docker pull command is used to pull an image from the ECR registry.