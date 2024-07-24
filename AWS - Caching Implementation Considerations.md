#AWS #ElastiCache #Storage 

- Read more at: https://aws.amazon.com/caching/implementation-considerations/
- Is it safe to cache data? Data may be out of date, eventually consistent
- Is caching effective for that data?  
    • Pattern: data changing slowly, few keys are frequently needed  
    • Anti patterns: data changing rapidly, all large key space frequently needed
- Is data structured well for caching?  
    • example: key value caching, or caching of aggregations results
- Which caching design pattern is the most appropriate?