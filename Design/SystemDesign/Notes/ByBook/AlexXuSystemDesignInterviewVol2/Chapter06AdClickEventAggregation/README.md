# Chapter 06. Ad Click Event Aggregation

## Step 1 - Understand the Problem and Establish Design Scope

TODO

### Functional Requirement

### Non-functional Requirement

### Back-of-the-envelope Estimation

## Step 2 - Propose High-Level Design and Get Buy-In

### Query API Design

### Data Model

#### Raw Data

#### Aggregated Data

#### Comparison

### Choose the Right Database

Canssandra

InfluxDB

Amazon S3 with Columnar data formats, like _ORC_, _Parquet_, or _AVRO_.

### High-Level Design

#### Asyncrhonous Processing

TODO

#### Aggregation Service

TODO

##### Map Reduce

###### Computing Unit

####### Map Node

####### Aggregate Node

####### Reduce Node

###### Main Use Cases

##### Use case 1: to aggregate the number of clicks

##### Use case 2: to return top N most clicked ads

##### Use case 3: data filtering

TODO

## Step 3, Design Deep Dive

### Streaming vs batching

TODO: pros and cons

Lambda Architecture

Kappa Architecture

#### Data Recalculation

#### Time

The timestamp can be generated in 2 different places:

- Event time: when ad ad click happens.
- Processing time: referes to the system time of the aggregation machine that processes the click event.

TODO: pros and cons

### Aggregation Window

4 types of window functions:

1. tumbling, also called fixed, window
2. hopping window
3. sliding window
4. session window

### Delivery guarantees

Message queues such as Kafka usually provide 3 delivery semantics:

1. at-most once
2. at-least once
3. exactly once

#### Which delivery method shall we choose?

### Data Deduplication

2 common sources:

- Client-side
- Server outage

### Scale the System

#### Scale the Message Queue

##### Producer

##### Consumer

##### Broker

###### Hashing Key

###### The Number of Partition

###### Topic Physical Sharding

### Scale the Aggregation Service

Option

- Allocate events with different *ad_id*s to different threads
- Deploy aggregate service nodes on resource providers like Apache Haddop YARN.
  - One can think of this approach as utilizing multi-processing.

### Scale the Database

#### Hotspot Issue

A shard or service that receives much more data than the others is called a hotspot.

### Fault Tolerance

### Data Monitoring and Correctness

#### Continuous Monitoring

Metrics to monitor:

- Latency
- Message queue size
- System resources on aggregation nodes

#### Reconciliation

Reconciliation means comparing different sets of data in order to ensure data integrity.

### Alternative Design

## Step 4, Wrap up
