#AWS #Networking #Route53 

• AWS Resources (Load Balancer, CloudFront...) expose an AWS hostname:
	• lb1-1234.us-east-2.elb.amazonaws.com and you want myapp.mydomain.com

• CNAME:  
	• Points a hostname to any other hostname. (app.mydomain.com => blabla.anything.com) 
	• ONLY FOR NON ROOT DOMAIN (aka. something.mydomain.com)

• Alias:
- Points a hostname to an AWS Resource (app.mydomain.com => blabla.amazonaws.com)
- Works for ROOT DOMAIN and NON ROOT DOMAIN (aka mydomain.com)
- Free of charge
- Native health check