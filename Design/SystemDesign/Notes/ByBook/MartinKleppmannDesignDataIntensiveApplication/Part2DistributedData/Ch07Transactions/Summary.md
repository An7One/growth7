# Chapter07, Transactions

## Summary

| Annotation                      | Explaination                                                                                                                                                                                               | Remedy                                                                                                                                                                                                                            |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Dirty reads                     | One client reads another client's writes before they have been committed.                                                                                                                                  | The read committed isolation level and strong levels prevent dirty reads.                                                                                                                                                         |
| Dirty writes                    | One client overwrites data that another client has written, but not yet committed.                                                                                                                         | Almost all transaction implementations prevent dirty writes.                                                                                                                                                                      |
| Read skew (nonrepeatable reads) | A client sees different parts of the database at different points in time.                                                                                                                                 | This issue is most commonly prevented with the snapshot isolation, which allows a transaction to read from a consistent snapshot at one point in time. It is usually implemented with _multi-version concurrency control_ (MVCC). |
| Lost updates                    | Two clients concurrently perform a read-modify-write cycle. One overwrites the other's write without incorporating its changes, so the data is lost.                                                       | Some implementations of the snapshot isolation prevent this anomaly automatically, while others require a manual lock (`SELECT FOR UPDATE`).                                                                                      |
| Write skew                      | A transaction reads something, makes a decision based on the value it saw, and writes the decision to the database. However, by the time the write is made, the premise of the decision is no longer true. | Only serialiable isolation prevents this anomaly.                                                                                                                                                                                 |
| Phantom reads                   | A transation reads objects that match some search condition. Another client makes a write that affects the results of that search.                                                                         | Snapshot isolation prevents straightfoward phantom reads, but phantoms in the context of write skew require special treatment, such as index-range locks.                                                                         |

### Consistency

| Model                                | Explaination | Example |
| ------------------------------------ | ------------ | ------- |
| Linearizability / Linear Consistency |              |         |
| Sequential Consistency               |              |         |
| Causual Consistency                  |              |         |
| PRAM/FIFO Consistency                |              |         |
| Eventual Consistency                 |              |         |

For eventual consistency

| Model                           | Explaination | Example |
| ------------------------------- | ------------ | ------- |
| Read-your-writes Consistency    |              |         |
| Monotonic-read Consistency      |              |         |
| Monotonic-write Consistency     |              |         |
| Writes-follow-reads Consistency |              |         |

### Serializability

SQL Isolation Levels (From strong to weak) - [Wiki](<https://en.wikipedia.org/wiki/Isolation_(database_systems)#Isolation_levels>)

| Model                                      | Explanation |
| ------------------------------------------ | ----------- |
| Serializability / Serializable consistency |             |
| Repeatable Read                            |             |
| Read Committed                             |             |
| Read Uncommitted                           |             |

### Reference

[[Soul Orbit](http://r12f.com/posts/summarizing-consistency-model)] 一致性模型一句话总结
