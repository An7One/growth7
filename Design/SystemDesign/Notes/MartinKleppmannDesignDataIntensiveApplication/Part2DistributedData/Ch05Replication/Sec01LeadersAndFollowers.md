# Chapter 05, Replication
## Section 1, Leaders and Followers

### Synchronous versus Asynchronous Replication

| Type                     | Pros                                                                                                                                                                                                                    | Cons                                                                                                                                                                                      |
| :----------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Synchronous Replication  | <ul><li>Followers are guaranteed to have up-to-date copy of data, which is consistent with the leader.</li><li>If the leader suddenly fails, we can be sure that the data is still available on the follower.</li></ul> | <ul><li>If the follower does not respond, the write cannot be processed.</li><ul>                                                                                                         |
| Asynchronous Replication | <ul><li>Even if all followers have falled behind, the leader can continue processing writes</li></ul>                                                                                                                   | <ul><li>A write is not guranteed to be durable.</li><ul><li>If the leader fails and is not recoverable, any write that ahve not yet been replicated to followers are lost.</li></ul></ul> |


### Setting up New Followers

#### Conceptual Steps

<ol>
    <li>to take a consistent snapshot of the leader's database if possible, without taking a lock on the entire database</li>
    <li>to copy the snapshot to the new follower node</li>
    <li>to connect to the leader, from the follower, and request all the data chagnes that have happened since the snapshot was take</li>
    <ul><li>this requires that the snapshot is associated with an exact position in the leader's replication log</li></ul>
    <li>to <em>catch up</em> when the follower has processed the backlog of data changes since the snapshot</li>
</ol>


### Handling Node Outages

<p>Being able to reboot individual nodes without downtime is a big advantage for operations and maintenance.</p>
<p>The goal is </p>
<ul><li>to keep the system as a whole running despite individual node failure</li>
<li>to keep the impact of a node outage as small as possible</li></ul></p>

#### Follower Failure: Catch-up Recovery

On its local disk, each follower keeps a log of the data changes it has received from the leader.

#### Leader Failure: Failover

Failover can happen mannually or automatically. An automatic failover process usually consists of the following steps:
<ol>
    <li>to determine that the leader has failed</li>
    <li>to choose a new leader</li>
    <li>to reconfigure the system to use the new leader</li>
</ol>

Failover is fraught with thigns that can go wrong:
<ul>
    <li>if asynchronous replication is used, the new leader many not have received all the writes from the old leader before it failed</li>
    <li>discarding writes is especially dangerous if other storage systems outside of the database need to be coordinated with the database contents</li>
    <li>split brain</li>
    <li>lack of proper timeout</li>
</ul>

### Implementation of Replication Logs

#### Statement-based replication

#### Write-ahead log(WAL) shipping

#### Logical (row-based) replication

#### Trigger-based replication