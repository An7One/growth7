# Chapter 05, Replication
## Section 3, Multi-Leader Replication

### Use cases
#### Multi-datacenter operation
| Item                           | Single Leader | Multiple Leaders |
| ------------------------------ | ------------- | ---------------- |
| Performance                    |               |                  |
| Tolerance of datacenter outage |               |
| Tolerance of network problems  |               |

#### Clients with offline operation

#### Collaborative Editting

### Handling Write Conflicts
#### Synchronous v.s. Asynchronous conflic detection
#### Conflict avoidance
#### Converging toward a consistent state
#### Custom conflict resolution logic

### Multi-Leader Replication Toplogies
A replication topology decribes the communication paths along which writes are propagated from one node to another.
<ul>
    <li>All-to-all Topology (most general)</li>
    <li>Star Topology</li>
    <li>Circular Topology</li>
</ul>