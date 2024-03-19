#ElastiCache #Storage 

**Pros**:  
	• Data in cache is never stale, reads are quick
	• Write penalty vs Read penalty (each write requires 2 calls)

**Cons**:
	• Missing Data until it is added / updated in the DB. Mitigation is to implement Lazy Loading strategy as well
	• Cache churn – a lot of the data will never be read
	
![[Captura de pantalla 2024-03-13 a la(s) 12.47.38 p.m..png]]
![[Captura de pantalla 2024-03-13 a la(s) 12.48.27 p.m..png]]
