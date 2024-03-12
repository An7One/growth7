# Chapter 04, Distributed Message Queue

## Step 1, Understand the Problem and Establish Design Scope

## Step 2, Propose High-Level Design and Get Buy-n

### Messaging Models

#### Point-to-point

#### Publish-subscribe

##### Topics, partitions, and brokers

##### Consumer group

### High-Level Architecture

TODO

## Step 3, Design Deep Dive

### Data storage

Option:

- Database
- Write-ahead log (WAL)
  - TODO: to connect with DDIA chapter 2

#### A note on disk performance

### Message data structure

#### Message key

#### Message value

#### Other fields of a message

- Topic
- Partition
- Offset
- Timestamp
- Size
- Cyclic Redundancy Check (CRC)

### Batching

#### Producer flow

#### Consumer flow

##### Push vs Pull

TODO: pros vs cons in comparisons

###### Push model

###### Pull model

##### Consumer rebalancing

### State storage

What to store:

- the mapping between partitions and consumers.
- the last consuemd offsets of consume groups for each partition.

The data access patterns for consumer states are:

- frequent read and write operations but the volume is not high
- data is updated frequently and is rarely deleted
- random read and write operations
- data consistency is important

### Metadata storage

#### Zookeeper

### Replication

TODO: to connect to the notes of DDIA chapter 5

#### In-sync replicas (ISR)

### Scalability

#### Producer

#### Consumer

#### Broker

#### Partition

##### Increase the number of partitions

- persisted messages still are in the old partitions, so there is no data migration.
- after the new partition is added, new messages will be persistened in all 3 partitions.

##### Decrease the number of partitions

- the partition-3 is decommissioned so new messages are only received by the remaining partitions
- the decommissioned partition, partition-3, cannot be removed immediately because data might be currently consumed by consumers for a certain amount of time. Only after the configured retention period passes, data can be truncated and storage space is freed up. Reducing partitions is **not** a shortcut to reclaiming data space.
- during this transitional period, while partion-3 is decommissioned, producers only send messages to the remaining 2 partitions, but consumers still can consume from all 3 partitions. After the retention period of the decommissioned partition expires, consumer groups need rebalancing.

### Data delivery semantics

#### At-most once

How it works at a high level:

- the producer sends a message asynchronously to a topic without waiting for an acknowledgement (ack = 0). If the message delivery fails, there is **no** retry.
- consumer fetches the message and commits the offset before the data is processed. If the consumer crashes just after the offset commit, the message will **not** be re-consumed.

#### At-least once

TODO

#### Exactly once

TODO

### Advanced features

#### Message filtering

#### Delayed messages & Scheduled messages

## Step 4, Wrap up
