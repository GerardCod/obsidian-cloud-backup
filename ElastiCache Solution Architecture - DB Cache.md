#ElastiCache #Storage 

- Applications queries ElastiCache, if not available, get from RDS and store in ElastiCache.
- Helps relieve load in RDS
- Cache must have an invalidation strategy to make sure only the most current data is used in there.

![[Captura de pantalla 2024-03-13 a la(s) 12.28.32 p.m..png]]