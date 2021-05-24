# Distributed Rate Limiter

### Why Rate Limiting is Needed?

<ul>
    <li>to prevent resource starvation</li>
    <li>to manage policies and quotas</li>
    <li>to control flow</li>
    <li>to avoid excess costs</li>
</ul>

### Strategy

<ul>
    <li>no rate limiting</li>
    <li>pass through</li>
    <li>to enforce rate limits</li>
    <li>to defer response</li>
</ul>

### Requirement

### Algorithm

<ul>
    <li>Token bucket</li>
    <li>Leaky bucket</li>
    <li>Sliding log</li>
    <li>Fixed window</li>
    <li>Sliding window</li>
</ul>

### Distributed Rate Limiter

<ul>
    <li>Load balancer</li>
    <li>Central storage, eg. Redis</li>
    <li>Optimized way based on central storage</li>
</ul>

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

[Google Cloud](https://cloud.google.com/architecture/rate-limiting-strategies-techniques) - Rate-Limiting strategies and technique

[Stripe Engineering Blog](https://stripe.com/blog/rate-limiters) - Scaling your API with rate limiters, by Paul Tarjan

[Github Engineering Blog](https://github.blog/2021-04-05-how-we-scaled-github-api-sharded-replicated-rate-limiter-redis/) - How we scaled the GitHub API with a sharded, replicated rate limiter in Redis, by Robert Mosolgo

[src](https://guanhonly.github.io/2020/05/30/distributed-rate-limiter/) - 如何设计一个分布式限流器(distributed rate limiter)