# Chapter07, Transactions
## Summary

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

SQL Isolation Levels (From strong to weak) ([Wiki] - https://en.wikipedia.org/wiki/Isolation_(database_systems)#Isolation_levels)

| Model                                      | Explanation |
| ------------------------------------------ | ----------- |
| Serializability / Serializable consistency |             |
| Repeatable Read                            |             |
| Read Committed                             |             |
| Read Uncommitted                           |             |

### Reference

[[Soul Orbit](http://r12f.com/posts/summarizing-consistency-model)] 一致性模型一句话总结