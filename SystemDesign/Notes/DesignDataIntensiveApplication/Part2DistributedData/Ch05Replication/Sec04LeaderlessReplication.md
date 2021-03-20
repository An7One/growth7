# Chapter 05, Replication
## Section 4, Leaderless Replication

### Writing to the database when a node is down

#### Read repair and anti-entropy
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