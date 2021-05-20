# Distributed Rate Limiter

### Requirement

### Algorithm

#### Token Bucket

#### Leaky Bucket

FIFO

#### Fixed Window

#### Sliding Window Log

to track timestamp

#### Sliding Window Counter

### Synchronization Policy

### Race Conditions

### Optimizing for Performance

latency


#### Message Broadcasting

<ul>
    <li>Tell everyone everything</li>
    <li>Gossip communication</li>
    <li>Distributed cache</li>
    <li>Coordination service</li>
    <li>Random leader selection</li>
</ul>


### Reference

[Youtube](https://youtu.be/FU4WlwfS3G0) System Design Interview - Rate Limiting (local and distributed)

[GitHub Blog](https://github.blog/2021-04-05-how-we-scaled-github-api-sharded-replicated-rate-limiter-redis/) How we scaled the GitHub API with a sharded, replicated rate limiter in Redis

[konghq](https://konghq.com/blog/how-to-design-a-scalable-rate-limiting-algorithm/) How to Design a Scalable Rate Limiting Algorithm