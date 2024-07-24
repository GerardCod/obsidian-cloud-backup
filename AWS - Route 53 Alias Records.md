#AWS #Networking #Route53 

- Maps a hostname to an AWS resource
- An extension to DNS functionality
- Automatically recognizes changes in the resource’s IP addresses
- Unlike CNAME, it can be used for the top node of a DNS namespace (Zone Apex), e.g.: example.com
- Alias Record is always of type A/AAAA for AWS resources (IPv4 / IPv6)
- You can’t set the TTL.

![[Captura de pantalla 2024-03-13 a la(s) 4.44.39 p.m..png]]