___
#flashcards/ComArk/7_Memory-Hierarchy

What is the difference between volatile and nonvolatile memory?
?
Volatile memory like RAM loses its contents when power is off, whereas nonvolatile memory like SSDs and HDDs retains data.
<!--SR:!2025-06-27,30,283-->

Why is DRAM more suited for main memory than SRAM?
?
DRAM is slower and needs refreshing but is cheaper and more compact, making it practical for large main memory. SRAM is faster but expensive and power-hungry, suitable for small CPU caches.
<!--SR:!2025-07-24,48,268-->

How does the DRAM structure store data?
?
DRAM stores bits in capacitors controlled by transistors, arranged in a matrix of rows and columns. Multiple banks are combined to form a full memory module.
<!--SR:!2025-06-24,18,203-->

What causes the majority of memory access delay?
?
The initial access latency dominates memory access time, more than the actual data transfer.
<!--SR:!2025-07-14,38,243-->

Why are caches organized hierarchically in modern CPUs?
?
To balance speed, cost, and space: small, fast caches are kept close to the CPU, while larger, slower caches are used further away.
<!--SR:!2025-07-21,45,263-->

What does the cache hit rate indicate?
?
It measures the percentage of memory accesses served by the cache, a key performance indicator for cache efficiency.
<!--SR:!2025-06-25,28,283-->

What is the Least Recently Used (LRU) replacement strategy?
?
LRU evicts the data that hasn’t been accessed for the longest time, approximating the optimal strategy without requiring future knowledge.
<!--SR:!2025-06-28,31,243-->

What is the Resource Augmentation Guarantee for LRU?
?
LRU performs at most twice as poorly as the optimal strategy if it has twice the cache size.
<!--SR:!2025-06-27,21,223-->

What are the pros and cons of direct-mapped caching?
?
**Pros**: Simple, fast, cheap.
**Cons**: High conflict rate, limited flexibility, potential thrashing, no performance guarantees.
<!--SR:!2025-06-19,29,283-->

How does fully associative mapping differ from direct mapping?
?
Fully associative caches allow any memory block to be placed in any cache line, reducing conflict misses but requiring expensive hardware for lookups.
<!--SR:!2025-06-23,17,190-->

What is k-way associative mapping in cache memory?
?
It divides the cache into sets with $k$ blocks each. A memory block maps to a set and can be placed in any of the $k$ blocks within it—offering a balance between flexibility and cost, by combining fully associative and direct mapping.
<!--SR:!2025-07-02,16,223-->

What is the difference between write-through and write-back caching?
?
Write-through updates cache and main memory simultaneously, ensuring consistency but increasing traffic. Write-back updates only the cache and writes to memory later, improving speed but requiring extra logic to track changes.
<!--SR:!2025-07-07,31,243-->
