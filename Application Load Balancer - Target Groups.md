#ALB #High_Availabilty 

• EC2 instances (can be managed by an Auto Scaling Group) – HTTP • ECS tasks (managed by ECS itself) – HTTP  
• Lambda functions – HTTP request is translated into a JSON event • IP Addresses – must be private IPs
• ALB can route to multiple target groups  
• Health checks are at the target group level

![[Captura de pantalla 2024-03-13 a la(s) 10.58.27 a.m..png]]

## Good to know

• Fixed hostname (XXX.region.elb.amazonaws.com)
• The application servers don’t see the IP of the client directly  
• The true IP of the client is inserted in the header X-Forwarded-For  
• We can also get Port (X-Forwarded-Port) and proto (X-Forwarded-Proto)