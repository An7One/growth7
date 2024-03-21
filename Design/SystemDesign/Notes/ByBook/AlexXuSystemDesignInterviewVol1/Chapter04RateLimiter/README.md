# Chapter 04: Design a Rate Limiter

## Introduction

Benefits with an API rate limiter

- to prevent resource starvation caused by Denial of Service (DoS) attack
- to reduce cost
- to prevent servers from being overloaded

## Step 1 - Understand the Problem and Establish Design Scope

### Functional Requirement

TODO

### Non-functional Requirement

TODO

### Estimation

TODO

### Summary of Requirements - TODO to be put into the above categories

- accurately limit exccessive requests
- low latency.
  - the rate limiter should not slow down HTTP response time
- use as little memory as possible
- distributed rate limiting.
  - the rate limiter can be shared across multiple servers or processes
- exception handling
  - show clear exceptions to users when their requests are throttled
- high fault tolerance

## Step 2 - Propose High-level Design and Get Buy-in

### Where to put the rate limiter?

- client-side implementation
- server-side implementation

### Algorithm for Rate Limiting

- Token Bucket
  - TODO
- Leaking Bucket
  - TODO
- Fixed Window Counter
  - TODO
- Sliding Window Log
  - TODO
- Sliding Window Counter
  - TODO

TODO

### High-level Architecture

- In-memory cache is picked because it is fast and supports time-based expiration strategy.

TODO

## Step 3 - Design Deep Dive

### Rate Limiting Rules

### Exceeding the Rate Limit

#### Rate Limiter Headers

### Detailed Design

### Rate Limiter in a Distributed Environment

TODO

#### Race Condition

TODO

#### Synchronization Issue

TODO

### Performance Optimization

TODO

### Monitoring

TODO

## Step 4 - Wrap Up

TODO
