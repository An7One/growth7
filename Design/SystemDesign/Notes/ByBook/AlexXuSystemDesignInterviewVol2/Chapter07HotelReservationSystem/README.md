# Chapter 07: Hotel Reservation System

## Step 1 - Understand the Problem and Establish Design Scope

### Functional Requirement

TODO

### Non-functional Requirement

TODO

### Estimation

TODO

## Step 2 - Propose High-level Design and Get Buy-in

### API Design

TODO

### Data Model

TODO

### High-level Design

TODO graph

## Step 3 - Design Deep Dive

### Improved Data Model

TODO

(What are the improvements)

### Concurrency Issue

2 common approaches:

- Client implementation
  - TODO
- API solution
  - TODO

3 options

- Pessimistic locking
  - also called pessimistic concurrency control, prevents simultaneous updates by placing a lock on a record as soon as one starts to update it.
  - others who attempt to update the record have to wait until the 1st user has released the lock (committed the change).
- Optimistic locking
  - TODO
- Database constraints
  - TODO

| option              | pro                                                                                                                                                                                                                | con                                                                                                                                                    |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| pessimistic locking | 1. prevents applications from updating data that is being, or has been, changed; 2. easy to implement, and it avoids conflicts by serializing updates. Pessimistic locking is useful when data contention is heavy | 1. Deadlocks may occur when multiple resources are locked. Writing deadlock-free application code could be challenging; This approach is not scalable. |
| optimistic locking  | 1. prevents applications from editing stale data; 2. no need to lock the database resource; 3. generally used when the data contention is low.                                                                     | Performance is poor when data contention is heavy.                                                                                                     |
| database constraint | 1. easy to implement; 2. works well when data contention is minimal                                                                                                                                                | 1. TODO; 2. cannot be version-controlled easily like the application code; 3. not all databases support constraints.                                   |

### Scaling the System

#### Database Sharding

TODO

#### Caching

TODO

##### New challenges posed by the cache

TODO

##### Data consistency among services

TODO

### Resolving data inconsistency in the microservice architecture

TODO

## Step 4 - Wrap Up

TODO
