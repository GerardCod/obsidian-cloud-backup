#ELB #High_Availabilty #Scalability

• Spread load across multiple downstream instances  
• Expose a single point of access (DNS) to your application • Seamlessly handle failures of downstream instances  
• Do regular health checks to your instances  
• Provide SSL termination (HTTPS) for your websites  
• Enforce stickiness with cookies  
• High availability across zones 
• Separate public traffic from private traffic.

• An Elastic Load Balancer is a managed load balancer • AWS guarantees that it will be working.
• AWS takes care of upgrades, maintenance, high availability • AWS provides only a few configuration knobs.

• It costs less to setup your own load balancer but it will be a lot more effort on your end.

• It is integrated with many AWS offerings / services • EC2, EC2 Auto Scaling Groups, Amazon ECS.
• AWS Certificate Manager (ACM), CloudWatch.
• Route53,AWSWAF,AWSGlobalAccelerator.