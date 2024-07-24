#AWS #Networking #Route53 

• A – maps a hostname to IPv4
• AAAA – maps a hostname to IPv6
• CNAME – maps a hostname to another hostname
- The target is a domain name which must have an A or AAAA record
- Can’t create a CNAME record for the top node of a DNS namespace (Zone Apex)
- Example: you can’t create for example.com, but you can create for www.example.com
• NS – Name Servers for the Hosted Zone
	• Control how traffic is routed for a domain