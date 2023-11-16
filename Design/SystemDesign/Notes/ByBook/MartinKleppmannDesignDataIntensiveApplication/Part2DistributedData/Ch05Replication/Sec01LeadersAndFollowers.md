# Chapter 05, Replication

## Section 1, Leaders and Followers

### Synchronous versus Asynchronous Replication

| Type                     | Pros                                                                                                                                                                                                                    | Cons                                                                                                                                                                                      |
| :----------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Synchronous Replication  | <ul><li>Followers are guaranteed to have up-to-date copy of data, which is consistent with the leader.</li><li>If the leader suddenly fails, we can be sure that the data is still available on the follower.</li></ul> | <ul><li>If the follower does not respond, the write cannot be processed.</li><ul>                                                                                                         |
| Asynchronous Replication | <ul><li>Even if all followers have falled behind, the leader can continue processing writes</li></ul>                                                                                                                   | <ul><li>A write is not guranteed to be durable.</li><ul><li>If the leader fails and is not recoverable, any write that ahve not yet been replicated to followers are lost.</li></ul></ul> |

### Setting up New Followers

#### Conceptual Steps

1. to take a consistent snapshot of the leader's database if possible, without taking a lock on the entire database
2. to copy the snapshot to the new follower node
3. to connect to the leader, from the follower, and request all the data changes that have happened since the snapshot was take
   - this requires that the snapshot is associated with an exact position in the leader's replication log
4. to _catch up_ when the follower has processed the backlog of data changes since the snapshot

### Handling Node Outages

Being able to reboot individual nodes without downtime is a big advantage for operations and maintenance.

The goal is

- to keep the system as a whole running despite individual node failure
- to keep the impact of a node outage as small as possible

#### Follower Failure: Catch-up Recovery

On its local disk, each follower keeps a log of the data changes it has received from the leader.

#### Leader Failure: Failover

The process that, one of the followers needs to be promoted to be the new leader, clients need to reconfigured to send their writes to the new leader, and the other followers need to start consuming data changes from the new leader, is called **_failover_**.

Failover can happen manually or automatically. An automatic failover process usually consists of the following steps:

1. to determine that the leader has failed
2. to choose a new leader
3. to reconfigure the system to use the new leader

Failover is fraught with things that can go wrong:

- if asynchronous replication is used, the new leader may not have received all the writes from the old leader before it failed
- discarding writes is especially dangerous if other storage systems outside of the database need to be coordinated with the database contents
- split brain
- lack of proper timeout

### Implementation of Replication Logs

#### Statement-based replication

#### Write-ahead log(WAL) shipping

#### Logical (row-based) log replication

#### Trigger-based replication
