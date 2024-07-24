#AWS #ElastiCache #Storage 

**Pros**
- Only requested data is cached (the cache isn’t filled up with unused data)
- Node failures are not fatal (just increased latency to warm the cache)
    
**Cons**
- Cache miss penalty that results in 3 round trips, noticeable delay for that request
- Stale data: data can be updated in the database and outdated in the cache

![[Captura de pantalla 2024-03-13 a la(s) 12.45.11 p.m..png]]

![[Captura de pantalla 2024-03-13 a la(s) 12.45.49 p.m..png]]