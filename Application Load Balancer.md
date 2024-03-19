#ALB #High_Availabilty 

- Application load balancers is Layer 7 (HTTP)
- Load balancing to multiple HTTP applications across machines (target groups)
- Load balancing to multiple applications on the same machine (ex: containers)
- Suppor t for HTTP/2 and WebSocket
- Support redirects (from HTTP to HTTPS for example)
- Routing tables to different target groups:
    • Routing based on path in URL (example.com/users & example.com/posts)
    • Routing based on hostname in URL (one.example.com & other.example.com)
    • Routing based on Query String, Headers (example.com/users?id=123&order=false)
- ALB are a great fit for micro services & container-based application (example: Docker & Amazon ECS)
- Has a port mapping feature to redirect to a dynamic port in ECS
- In comparison, we’d need multiple Classic Load Balancer per application![[Captura de pantalla 2024-03-13 a la(s) 10.56.09 a.m..png]]