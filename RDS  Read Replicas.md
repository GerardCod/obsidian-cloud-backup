#RDS #Storage 

- Up to 15 Read Replicas
- Within AZ, Cross AZ or Cross Region
- Replication is ASYNC, so reads are eventually consistent
- Replicas can be promoted to their own DB 
- Applications must update the connection string to leverage read replicas

![[Captura de pantalla 2024-03-13 a la(s) 11.49.47 a.m..png]]
