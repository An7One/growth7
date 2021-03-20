# Chapter 05, Replication

## Leaders and Followers

### Synchronous versus Asynchronous Replication

| Type                     | Pros                                                                                                                                                                                                                    | Cons                                                                                                                                                                                      |
| :----------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Synchronous Replication  | <ul><li>Followers are guaranteed to have up-to-date copy of data, which is consistent with the leader.</li><li>If the leader suddenly fails, we can be sure that the data is still available on the follower.</li></ul> | <ul><li>If the follower does not respond, the write cannot be processed.</li><ul>                                                                                                         |
| Asynchronous Replication | <ul><li>Even if all followers have falled behind, the leader can continue processing writes</li></ul>                                                                                                                   | <ul><li>A write is not guranteed to be durable.</li><ul><li>If the leader fails and is not recoverable, any write that ahve not yet been replicated to followers are lost.</li></ul></ul> |
|                          |                                                                                                                                                                                                                         |


### Setting up new followers

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
<li>to keep the impact of a node outage as small as possible</li></ul>
#### Follower Failure: Catch-up Recovery
On its local disk, each follower keeps a log of the data changes it has received from the leader.
#### Leader Failure: Failover


### Implementation of Replication Logs
<ul>
    <li>State-based replication</li>
    <li>Row-based replication</li>
    <li>Trigger-based replication</li>
</ul>