#ElastiCache #Storage 

• Cache eviction can occur in three ways: 
• You delete the item explicitly in the cache
• Item is evicted because the memory is full and it’s not recently used (LRU) 
• You set an item time-to-live (or TTL)
• TTL are helpful for any kind of data: 
	• Leaderboards
	• Comments  
	• Activity streams
• TTL can range from few seconds to hours or days  
• If too many evictions happen due to memory, you should scale up or out