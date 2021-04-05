# Chapter 07, Transactions
## Section 03, Serializability

### Actual Serial Execution

#### Encapsulating transactions in stored procedures

#### Pros and cons of stored procedures

#### Partitioning

#### Summary of serial execution

### Two-Phase Locking (2PL)

#### Implementation of two-phase locking

#### Performance of two-phase locking

#### Predicate locks

#### Index-range locks

### Serializable Snapshot Isolation (SSI)

#### Pessimistic v.s. optimistic concurrency control

#### Decisions based on an outdated premise

#### Detecting stale MVCC reads

#### Detecting writes that affect prior reads

#### Performance of serializable snapshot isolation