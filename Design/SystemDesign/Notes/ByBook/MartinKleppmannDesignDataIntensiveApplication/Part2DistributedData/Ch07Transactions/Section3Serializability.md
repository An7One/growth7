# Chapter 07: Transactions

## Section 3 Serializability

Most databases that provide serializability today use one of 3 techniques:

1. literally executing transactions in a serial order
2. two-phase locking
3. optimistic concurrency control techniques such as serializable snapshot isolation

### Actual Serial Execution

TODO

#### Encapsulating transactions in stored procedures

TODO

#### Pros and cons of stored procedures

TODO

#### Paritioning

TODO

#### Summary of serial execution

TODO

### Two-Phase Locking (2PL)

TODO

#### Implementation of two-phase locking

TODO

#### Performance of two-phase locking

TODO

#### Predicate locks

TODO

#### Index-range locks

TODO

### Serializable Snapshot Isolation (SSI)

TODO

#### Pessimistic v.s. optimistic concurrency control

TODO

#### Decisions based on an outdated premise

TODO

#### Detecting stale MVCC reads

TODO

#### Detecting writes that affect prior reads

TODO

#### Performance of serializable snapshot isolation

TODO
