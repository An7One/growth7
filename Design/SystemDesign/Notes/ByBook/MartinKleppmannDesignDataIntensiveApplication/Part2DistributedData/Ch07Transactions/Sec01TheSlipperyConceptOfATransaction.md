# Chapter 07, Transactions

## The Slippery Concept of a Transaction

### The Meaning of ACID

- Atomicity
- Consistency
- Isolation
  - in the sense of ACID, means that concurrently executing transactions are isolated from each other: they cannot step on each other's toes.
  - the classic database textbooks formalize isolation as _serializability_, which means that each transaction can pretend that it is the only transaction running on the entire database.
  - the database ensures that when the transactions have committed, the result is the same as if they run _serially_ (one after another), even though they may have run concurrently
- Durability
  - is the promise that once a transaction has committed successfully, any data it has written will not be forgotten, even if there is a hardware fault or the database crashes

### Single-Object and Multi-Object Operations

#### Single-object writes

#### The need for multi-object transactions

#### Handling errors and aborts

## (<-correct?) Weak Isolation Levels

### Read Commiteed

It makes 2 guarantees:

- when reading from the database, one will only see data that has been committed (no dirty reads).
- when writing to the database, one will only overwirte data that has been committed (no dirty writes).

#### No dirty reads

Transactions running at the _read committed_ isolation level must prevent dirty reads. This means that any write by a transaction only becomes visible to others when that transation commits (and then all of tis writes become visible at once).

#### No dirty writes

#### Implementing read committed

### Snapshot Isolation and Repeatable Read

### Serializability

### Two-Phase Locking (2PL)

### Serializable Snapshot Isolation (SSI)

## Summary
