#ELB #High_Availabilty 

- AWS has 4 kinds of managed Load Balancers
- Classic Load Balancer (v1 - old generation) – 2009 – CLB • HTTP, HTTPS,TCP,SSL(secureTCP)
- Application Load Balancer (v2 - new generation) – 2016 – ALB • HTTP, HTTPS,WebSocket
- Network Load Balancer (v2 - new generation) – 2017 – NLB • TCP,TLS(secureTCP),UDP
- Gateway Load Balancer – 2020 – GWLB  
    • Operates at layer 3 (Network layer) – IP Protocol
- Overall, it is recommended to use the newer generation load balancers as they provide more features
- Some load balancers can be setup as internal (private) or external (public) ELBs