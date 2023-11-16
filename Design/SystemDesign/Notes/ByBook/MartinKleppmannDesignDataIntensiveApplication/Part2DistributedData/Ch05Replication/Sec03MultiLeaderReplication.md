# Chapter 05, Replication

## Section0 3, Multi-Leader Replication

### Use case for Multi-Leader Replication

#### Multi-datacenter operation

| Item                           | Single Leader                                                                                                                                                                                               | Multiple Leaders                                                                                                                                                                                                                    |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Performance                    | Every write must go over the Internet to the datacenter with the leader, which can adding significant latency to writes and might contravene the purpose of having multiple datacenters in the first place. | Every write can be processed in the local datacenter and is replicated asynchronously to the other datacenters. Thus, the inter-datacenter network delay is hidden from users, which means the perceived performance may be better. |
| Tolerance of datacenter outage | If the datacenter with the leader fails, failover can promote a follower in another datacenter to be leader.                                                                                                | Each datacenter can continue operating independently of the others, and replication catches up when the failed datacenter comes back online.                                                                                        |
| Tolerance of network problems  | Very sensitive to problems in this inter-datacenter link, because writes are made synchronously over this link.                                                                                             | Can usuaully tolerate network problems better: a temporary network interruption does not prevent writes from being processed.                                                                                                       |

#### Clients with offline operation

#### Collaborative editing

### Handling Write Conflicts

#### Synchronous v.s. Asynchronous conflic detection

#### Conflict avoidance

#### Converging toward a consistent state

#### Custom conflict resolution logic

### Multi-Leader Replication Toplogies

A replication topology describes the communication paths along which writes are propagated from one node to another.

- All-to-all Topology (most general)
- Star Topology
- Circular Topology
