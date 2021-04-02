# Chapter 07, Transactions
## Section 02, Weak Isolation Levels

### Read Committed
The most basic level of transcation isolation, which makes two guarantees
<ul>
    <li>When reading from the database, you will only see data that has been committed (no dirty reads)</li>
    <li>When writing to the database, you will only overwrite data that has been committed (no dirty writes)</li>
</ul>

### Snapshot Isolation and Repeatable Read
Snapshot isolation is that each transaction reads from a consistent snapshot of the database --- that is, the transaction sees all the data that was committed in the database at the start of the transaction. Even if the data is subsequently changed by another transaction, each transaction sees only the old data from that particular point in time.
#### Implementing snapshot isolation
#### Visibility rules for observing a consistent snapshot
#### Indexes and snapshot isolation
#### Repeatable read and naming confusion

### Preventing Lost Updates

#### Atomic write operations

#### Explicit locking

#### Automatically detecting lost updates

#### Compare-and-set

#### Conflict resolution and replication

### Write Skew and Phantoms

#### Characterizing write skew

#### More examples of write skew

#### Phantoms causing write skew

#### Materializing conflicts