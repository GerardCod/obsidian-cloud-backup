#Troubleshooting_and_Optimization #ElastiCache #Cache
## Question

You are creating a web application in which users can follow each other. Some users will be more popular than others and thus their data will be requested very often. Currently, the user data sits in RDS and it has been recommended by your Developer to use ElastiCache as a caching layer to improve the read performance. The whole dataset of users cannot sit in ElastiCache without incurring tremendous costs and therefore you would like to cache only the most often requested users profiles there. As your website is high traffic, it is accepted to have stale data for users for a while, as long as the stale data is less than a minute old.

## Solution

**Use a Lazy Loading strategy with TTL**

Lazy loading is a caching strategy that loads data into the cache only when necessary. Whenever your application requests data, it first requests the ElastiCache cache. If the data exists in the cache and is current, ElastiCache returns the data to your application. If the data doesn't exist in the cache or has expired, your application requests the data from your data store. Your datastore then returns the data to your application.

In this case, data that is actively requested by users will be cached in ElastiCache, and thanks to the TTL, we can expire that data after a minute to limit the data staleness.

![](https://assets-pt.media.datacumulus.com/aws-dva-pt/assets/pt5-q42-i1.jpg)