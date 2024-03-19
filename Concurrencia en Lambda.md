#Troubleshooting_and_Optimization #Lambda 

**Configura Application Auto Scaling para gestionar concurrencia provisional en un schedule**

Concurrencia es el número de peticiones que una función Lambda está funcionando a cualquier momento. Si una función Lambda es invocada nuevamente mientras una petición aún es procesada, otra instancia es reservada lo que incrementa la concurrencia de la función.

Due to a spike in traffic, when Lambda functions scale, this causes the portion of requests that are served by new instances to have higher latency than the rest. To enable your function to scale without fluctuations in latency, use provisioned concurrency. By allocating provisioned concurrency before an increase in invocations, you can ensure that all requests are served by initialized instances with very low latency.

You can configure Application Auto Scaling to manage provisioned concurrency on a schedule or based on utilization. Use scheduled scaling to increase provisioned concurrency in anticipation of peak traffic. To increase provisioned concurrency automatically as needed, use the Application Auto Scaling API to register a target and create a scaling policy.

Please see this note for more details on provisioned concurrency: ![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt2-q3-i1.jpg)
