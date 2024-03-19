# Chapter 05: Replication

## Section 4, Leaderless Replication

### Writing to the database when a node is down

#### Read repair and anti-entropy

The replication scheme should ensure that eventually all the data is copied to every replica.

To catch up on the writes missed, two mechanisms are often used in Dynamo-style datastores:

- Read repair
  - When a client makes a read from several nodes in parallel, it can detect any stale response.
  - This approach works well for values that are frequently read.
- Anti-entropy process
  - a background process that constantly looks for differences in the data between replicas and copies any missing data from one replica to another.
  - Does not copy writes in any particular order.
  - There might be significant delay before data is copied.

#### Quorums for reading and writing

### Limitations of Quorum Consistency

#### Monitoring staleness

### Sloppy Quorum and Hinted Handoff

#### Multi-datacenter operation

### Detecting Concurrent Writes

#### Last write wins (discarding concurrent writes)

To declare that each replica needs only to store the most "recent" value and allow "older" values to be overwritten and discarded.

TODO

#### The "happens-before" relationship and concurrency

#### Capturing the happens-before relationship

#### Merging concurrently written values

#### Version vectors
