# Chapter 01: Scale from Zero to Millions of Users

## Single Server Setup

## Database

### Which database to use?

## Vertical Scaling vs Horizontal Scaling

TODO - Limitations of the vertical scaling

## Load Balancer

## Database Replication

TODO - Pros vs Cons

## Cache

A cache is a temporary storage area that stores the result of expensive responses or frequently accessed data in memory so that subsequent requests are served more quickly.

### Cache Tier

The benefit of having a separate cache tier include better system performance, ability to reduce database workloads, and the ability to scale the cache tier independently.

### Consideration of Using Cache

- decide when to use cache
- expiration policy
- consistency
- mitigating failure
- evication policy

## Content Delivery Network (CDN)

TODO

### Consideration of using a CDN

- cost
- setting an appropriate cache expiry
- CDN fallback
- invalidting files

## Stateless Web Tier

### Stateful Architecture

TODO

### Stateless Architecture

TODO

## Data Centers

TODO

## Message Queue

TODO

## (<-?) Logging, Metric, Automation

TODO

## (<-?) Adding Message Queues and Different Tools

TODO

## Database Scaling

TODO

### Vertical Scaling

TODO

### Horizontal Scaling

- resharding data
- celebrity problem
- join and de-normalization

## Millions of Users and Beyond

- to keep web tier stateless
- to build redundancy at every tier
- to cache data as much as you can
- to support multiple data centers
- to host static assets in CDN
- to scale one's data tier by sharding
- to split tiers into individual services
- to monitor one's system, and use automation tools
