# Redis

### Why to pick Redis?

<ul>
    <li>Performance</li>
    <ul>
        <li>single process, single thread</li>
        <ul>
            <li>i/o multiplexing: epoll etc.</li>
        </ul>
        <li>in-memory</li>
        <li>asynchronous replication</li>
        <li>written in C</li>
    </ul>
    <li>Rich Primitives Support</li>
    <ul>
        <li>Key-Value Operations</li>
        <ul>
            <li>batching</li>
            <li>atomicity</li>
            <ul>
                <li>to execute singular commands is atomic</li>
                <li>to execute multiple commands is not atomic</li>
                <li>to pipeline is not atomic, but it is fast</li>
                <li><code>MULTI</code> is atomic, but one cannot chain results</li>
                <ul>
                    <li>transaction: <code>MULTI</code>, <code>EXEC</code>, <code>DISCARD</code>, <code>WATCH</code></li>
                    <ul>
                        <li>no interleaving</li>
                        <li>autofix after crash</li>
                        <li>will execute even there is failure on the sever side</li>
                        <li>optimistic locking: watch</li>
                    </ul>
                </ul>
                <li>Lua scripts are atomic and chainable</li>
            </ul>
            <li>multi-key</li>
            <li>eviction policy</li>
        </ul>
        <li>Data Structures</li>
        <ul>
            <li>String: counting</li>
            <ul>
                <li>Bitmap: real time metric, bloom filter</li>
            </ul>
            <li>List: stack, queue</li>
            <li>Hash: sessions</li>
            <li>Set, SortedSet: topN, pagination</li>
            <li>HyperLogLog: counting estimation</li>
        </ul>
        <li>Pub/Sub</li>
        <ul>
            <li>note: could receive the same message multiple times</li>
        </ul>
        <li>Distributed Lock</li>
        <ul>
            <li>safety, deadlock free, fault-tolerant</li>
            <li>set ex nx + compare and delete</li>
            <li>redlock?</li>
            <ul>
                <li>strong assumptions on clock, network, program</li>
                <li>anything could fail</li>
            </ul>
            <li>fencing: monotonicity</li>
            <ul>
                <li>Chubby: Sequencer</li>
                <ul>
                    <li>to ask Chubby server</li>
                    <li>to use generation number</li>
                    <li>to lock delay</li>
                </ul>
            </ul>
            <li>other implementations</li>
            <ul>
                <li>pre-fetch</li>
                <ul>
                    <li>smaller timeout</li>
                    <li>logical expire</li>
                </ul>
            </ul>
            <li>use cases</li>
            <ul>
                <li>synchronization: resource access</li>
                <li>thundering herd</li>
            </ul>
        </ul>
    </ul>
</ul>

### Patterns and Usages

### Redis Persistence

<ul>
    <li>AOF: Append Only File</li>
    <ul>
        <li>appendonly</li>
        <li>appendfsync</li>
        <li>cmd eg.: BGREWRITEAOF</li>
    </ul>
    <li>RDB: Redis Database Backup File</li>
    <ul>
        <li>cmd eg. Save "60 1000"</li>
        <ul>
            <li>rename</li>
        </ul>
    </ul>
</ul>

### Replication

### HA

### Sharding

### Operation Caveats

### Reference

[Youtube](https://youtu.be/fT4ogDNWsi0) - System Design-cache/系统设计-缓存/Redis: 理论与实践(基础)

[Youtube](https://youtu.be/YPtPz8I4c6U) - System Design-cache/系统设计-缓存/Redis: 理论与实践(进阶)

[WeChat Post](https://mp.weixin.qq.com/s/qGfAuS0e8dV77SRI3O3Q_w) - Redis 官方的高可用性解决方案

[cnblog](https://www.cnblogs.com/bingshu/p/9776610.html) - Redis（二）冰叔带你了解Redis-哨兵模式和高可用集群解析