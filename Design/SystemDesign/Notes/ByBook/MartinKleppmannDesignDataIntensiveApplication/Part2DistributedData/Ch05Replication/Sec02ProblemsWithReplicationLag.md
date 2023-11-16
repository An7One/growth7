# Chapter 05, Replication

## Section 02, Problems with Replication Lag

Leader-based replication requires all writes to go through a single node, but read-only queries can go to any replica.

If one stops writing to the database and waits a while, the followers will eventually catch up and become consistent with the leader. This effect is called _eventual consistency_.

### Reading Your Own Writes

### Monotonic Reads

### Consistent Prefix Reads

### Solutions for Replication Lag
