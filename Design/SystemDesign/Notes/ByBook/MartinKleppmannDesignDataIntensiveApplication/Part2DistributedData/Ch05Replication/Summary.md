# Chapter 05, Replication

## Summary

Replication can serve several purposes:

- High availability
  - to keep the system running, even when one or several mathines, or an entire datacenter goes down
- Disconnected operation
  - to allow an application to continue working when there is a network interruption
- Latency
  - to place data geographically close to users, so that users can interact with it faster
- Scalability
  - to be able to handle a higher volume of reads than a single machine could handle, by performing reads on replicas
