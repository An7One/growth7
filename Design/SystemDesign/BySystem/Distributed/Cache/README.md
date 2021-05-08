# Distributed Cache

### Requirements

#### Functional

<ul>
    <li>put(key, value)</li>
    <ul>
        <li>Distributed Hash Table</li>
    </ul>
    <li>get(key)</li>
</ul>

#### Non-Functional

<ul>
    <li>Scalablibility</li>
    <li>High Availability</li>
    <li>Fault-tolerance</li>
</ul>


#### What else is important

<ul>
    <li>Consistency</li>
    <li>Data expiration</li>
    <li>Local and remote cache</li>
    <li>Security</li>
    <li>Monitoring and logging</li>
    <li>Cache client</li>
    <li>Consistent hashing</li>
    <ul>
        <li>Domino effect</li>
    </ul>
</ul>

### Use Case

<ol>
    <li>Database Caching</li>
    <li>User Sessions Storing</li>
    <li>In-memory Data Lookup</li>
    <li>Cross-Module Communication & Shared Storage</li>
</ol>

### Algorithm

#### Cache Invalidation

<ul>
    <li>Cache Aside</li>
    <li>Read-Through</li>
    <ul>
        <li>to maintain the complete data consistency between the cache and the main storage</li>
        <li>Higher Latency</li>
    </ul>
    <li>Write-Through</li>
    <ul>
        <li>"cache miss"</li>
    </ul>
    <li>Write-Back</li>
    <ul>
        <li>Pros</li>
        <ul>
            <li>Low Latency</li>
            <li>High Throughput</li>
        </ul>
        <li>Cons</li>
        <ul>
            <li>Risk of data loss in case of a crash or other adverse event, because the only copy of the written data is in the cache</li>
        </ul>
    </ul>
    <li>Write-Around</li>
</ul>

#### Cache Eviction Policies

<ol>
    <li>First In First Out (FIFO)</li>
    <li>Last In First Out (LIFO)</li>
    <li>Least Recently Used (LRU)</li>
    <li>Most Recently Used (MRU)</li>
    <li>Least Frequently Used (LFU)</li>
    <li>Random Replacement</li>
</ol>

### Some Popular Distributed Chaches

<ul>
    <li>Eh-cache</li>
    <li>Memcache</li>
    <li>Redis</li>
    <li>Riak</li>
    <li>Hazelcast</li>
</ul>


### Reference:
[Youtube](https://youtu.be/iuqZvajTOyA) System Design Interview - Distributed Cache

[Youtube](https://youtu.be/DUbEgNw-F9c) Redis system design | Distributed cache system design

[Medium](https://medium.com/rtkal/distributed-cache-design-348cbe334df1) Distributed Cache Design

[8bitmen](https://www.8bitmen.com/distributed-cache-101-the-only-guide-youll-ever-need/) Distributed Cache 101

[Youtube](https://youtu.be/UH7wkvcf0ys) Facebook and memcached - Tech Talk