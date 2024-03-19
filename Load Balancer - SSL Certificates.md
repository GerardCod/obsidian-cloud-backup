#High_Availabilty #Encryption 

• The load balancer uses an X.509 certificate (SSL/TLS server certificate) 
• You can manage certificates using ACM (AWS Certificate Manager)  
• You can create upload your own certificates alternatively
• HTTPS listener:  
	• You must specify a default certificate
	• You can add an optional list of certs to support multiple domains  
	• Clients can use SNI (Server Name Indication) to specify the hostname they reach  
	• Ability to specify a security policy to support older versions of SSL /TLS (legacy clients)