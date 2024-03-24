# Chapter 9: Consistency and Consensus

## Section 4 Distributed Transactions and Consensus

There are a number of situations in which it is important for nodes to agree.

- Leader election
- Atomic commit

### Atomic Commit and Two-Phase Commit (2PC)

#### From single-node to distributed atomic commit

#### Introduction to two-phase commit

Instead of a single commit request, as with a single-node transaction, the commit/abort proces in 2PC is split into two phases, hence the name.

TODO - coordinator

TODO - main steps

#### A system of promises

TODO - main steps

#### Coordinator failure

TODO

#### Three-phase commit

TODO

### Distributed Transactions in Practice

TODO

#### Exactly-once message processing

TODO

#### XA transactions

TODO

#### Holding locks while in doubt

TODO

#### Recovering from coordinator failure

TODO

#### Limitations of distributed transactions

TODO

### Fault-Tolerant Consensus

#### Consensus algorithms and total order broadcast

#### Single-leader replication and consensus

#### Epoch numbering and quorums

#### Limitations of consensus

### Membership and Coordination Services

#### Allocating work to nodes

#### Service discovery

#### Membership services
