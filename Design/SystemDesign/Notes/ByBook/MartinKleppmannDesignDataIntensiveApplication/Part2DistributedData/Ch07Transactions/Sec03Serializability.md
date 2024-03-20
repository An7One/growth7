# Chapter 07: Transactions

## Section 03. Serializability

Most databases that provide serializability today use one of 3 techniques:

1. literally executing transactions in a serial order
2. two-phase locking
3. optimistic concurrency control techniques such as serializable snapshot isolation

### Actual Serial Execution

#### Encapsulating transactions in stored procedures

#### Pros and cons of stored procedures

#### Paritioning

#### Summary

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
