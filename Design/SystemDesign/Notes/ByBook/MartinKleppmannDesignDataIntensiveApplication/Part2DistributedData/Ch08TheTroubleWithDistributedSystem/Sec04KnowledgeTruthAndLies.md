# Chapter 08, The Trouble with Distributed Systems

## Section 04, Knowledge, Truth, and Lies

### The Truth Defined by the Majority

### Byzantine Faults

Distributed system problems become much harder if there is a risk that nodes may "lie" (send arbtrary faulty or corrupted responses). Such behavior is known as a _Byzantine fault_, and the problem of reaching consensus in this untrusting environment is know as the _Byzantine Generals Problem_.

### System Model and Reality

With regard to timing assumptions:

- Synchronous model
- Partially synchronous model
- Asynchronous model

With regard to nodes:

- Crash-stop faults
- Crash-recovery faults
- Byzantine (arbitrary) faults

#### Correctness of an algorithm

- Uniqueness
- Monotonic sequence
- Availability

#### Safety and liveness

#### Mapping system models to the real world
