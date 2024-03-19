#Aurora #High_Availabilty #Scalability 

- 6 copies of your data across 3 AZ:  
    • 4 copies out of 6 needed for writes  
    • 3 copies out of 6 need for reads  
    • Self healing with peer-to-peer replication • Storage is striped across 100s of volumes
- One Aurora Instance takes writes (master)
- Automated failover for master in less than 30 seconds
- Master + up to 15 Aurora Read Replicas serve reads
- Support for Cross Region Replication

![[Captura de pantalla 2024-03-13 a la(s) 12.17.42 p.m..png]]