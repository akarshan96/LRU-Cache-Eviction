# LRU-Cache-Eviction

When we Google __best cache eviction policy__, we get __LRU__ which is an abbreviation of __Least Recently Used__ as the top search result. In this blog, I am gonna decode LRU Cache Eviction Policy. Let's start by understanding the core goal for any cache eviction algorithm. 

###1. The Goal###
The goal for any cache eviction algorithm or technique is to improve cache performance by ensuring the most commonly accessed resources in the application remain in the cache memory while the other resources get evicted. In this way, commonly accessed resources can be retrieved by the user or application modules almost instantaneously which reduces the no. of expensive repetitive queries and improves the overall performance of the application in turn. The cache eviction algorithm or policy is responsible to remove or evict data from the cache when it's full. LRU is one of the cache eviction policy.

###2. The Defination###
In LRU, as the name suggests the least recently used resource or data gets evicted from the cache when it's full. 
For example, if we have a cache with a capacity of 3 items. First, we add an element 7, since the cache's max capacity is not reached, 7 can easily be accommodated inside cache. 

![](https://thepracticaldev.s3.amazonaws.com/i/jrfo0kk4hsy4c4lnfwoo.JPG)

Same will happen with the next two elements 2 and 9. 

![](https://thepracticaldev.s3.amazonaws.com/i/teg07x4bkq7qlla0316r.JPG)

Now when we add next element say 5, as the max capacity of cache, is already reached, we need to evict least recently used element that is 7 and add 5. This is similar to __Queue__ data structure since we are following FIFO.

![](https://thepracticaldev.s3.amazonaws.com/i/xnyh1pehr90fqoslj5l4.JPG)

If we have got 7 in place of 5 the 7 would have come in the front of the queue since it's recently used.

Read more from [my blog](https://dev.to/akarshan96/implementing-least-recently-used-cache-eviction-policy-2odn)
