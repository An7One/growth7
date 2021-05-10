# Notification Service

### Requirement

#### Functional

<ul>
    <li>createTopic(topicName)</li>
    <li>publish(topicName, message)</li>
    <li>subscribe(topicName, endpoint)</li>
</ul>

#### Non-Functional

<ul>
    <li>Scalable (supports an arbitrarily large numnber of topics, publishers and subscribers)</li>
    <li>Highly Available (survies hardware/network failures, no single point of failure)</li>
    <li>Highly Performant (keep end-to-end latency as low as possible)</li>
    <li>Durable (messages must not be lost, each subscriber must receive every message at least once)</li>
</ul>

### Reference:

[Youtube 20190328](https://youtu.be/bBTPZ9NdSk8) - System Design Interview - Notfication Service

[Youtube 20181109](https://youtu.be/6w6E_B55p0E) - Scaling Push Messaging for Millions of Devices @Netflix