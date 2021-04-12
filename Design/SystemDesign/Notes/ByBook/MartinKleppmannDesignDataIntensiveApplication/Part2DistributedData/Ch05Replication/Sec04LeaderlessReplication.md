# Chapter 05, Replication
## Section 4, Leaderless Replication

### Writing to the database when a node is down

#### Read repair and anti-entropy
<p>The replication scheme should ensure that eventually all the data is copied to every replica.</p>
To catch up on the writes missed, two mechanisms are often used in Dynamo-style datastores:
<ul>
    <li>Read Repair</li>
    <ul>
        <li>When a client makes a read from several nodes in parallel, it can detect any stale response.</li>
        <li>This approach works well for values that are frequently read.</li>
    </ul>
    <li>Anti-entropy process</li>
    <ul>
        <li>a background process that constantly looks for differences in the data between replicas and copies any missing data from one replica to another.</li>
        <li>Does not copy writes in any particular order.</li>
        <li>There might be significant delay before data is copied.</li>
    </ul>
</ul>

#### Quorums for reading and writing

### Limitations of Quorum Consistency

#### Monitoring staleness

### Sloppy Quorum and Hinted Handoff

#### Multi-datacenter operation

### Detecting Concurrent Writes
#### Last write wins(discarding concurrent writes)
#### The "happens-before" relationship and concurrency
#### Capturing the happens-before relationship
#### Merging concurrently written values
#### Version vectors