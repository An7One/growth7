# Chapter 01 Escaping Monolithic Hell

## 1.1 The Slow March Toward Monolithic Hell

### 1.1.1 The architecture of the FTGO application

### 1.1.2 The benefits of the monolithic architecture

<ul>
    <li>Simple to develop</li>
    <li>Easy to make radical changes to the application</li>
    <li>Straighforward to test</li>
    <li>Straightforward to deploy</li>
    <li>Easy to scale</li>
</ul>

### 1.1.3 Living in monolithic hell

<ul>
    <li>Complexity intimidates developers</li>
    <li>Development is slow</li>
    <li>Path from commit to deployment is long and arduous</li>
    <li>Scaling is difficult</li>
    <li>Devlivering a reliable monolith is chanlleging</li>
    <li>Locked into increasingly obsolete technology stack</li>
</ul>

## 1.2 Why is this Book Relevant to you

## 1.3 What will one Learn in this Book

## 1.4 Microservice Architecture to the Rescue

### 1.4.1 Scale Cube and Microservices

<ul>
    <li>X-axis scaling load balances requests across multiple instances</li>
    <li>Z-axis scaling routes requests based on an attribute of the request</li>
    <li>Y-axis scaling functionally decomposes an application into services</li>
    <ul>
        <li>
            A <i>service</i> is a mini application that implements narrowly focused functionality.
        </li>
    </ul>
</ul>

### 1.4.2 Microservices as a Form of Modularity

<i>Modularity</i> is essential when developing larget, complex applications.

### 1.4.3 Each Service has its Own Database

### 1.4.4 The FTGO Microservice Architecture

### 1.4.5 Comparing the Microservice Architecture and SOA

|                             | SOA                                    | Microservices                       |
| --------------------------- | -------------------------------------- | ----------------------------------- |
| Inter-service Communication | Smart pipes                            | Dumb pipes                          |
| Data                        | Global data model and shared databases | Data model and database per service |
| Typical Service             | Larger monolithic application          | Smaller service                     |

## 1.5 Benefits and Drawbacks of the Microservice Architecture

### 1.5.1 Benefits of the Microservice Architecture

<ul>
    <li>It enables the continous delivery and deployment of large, complex applications</li>
    <li>Services are small and easily maintained</li>
    <li>Services are independently deployable</li>
    <li>Services are independently scalable</li>
    <li>The microservice architecture enables teams to be autonomous.</li>
    <li>It allows easy experimenting and adoption of new technologies</li>
    <li>It has better fault isolation</li>
</ul>

### 1.5.2 Drawbacks of the Microservice Architecture

<ul>
    <li>Finding the right set of services is challenging</li>
    <li>Distributed systems are complex, which makes development, testing, and deployment difficult</li>
    <li>Deploying features that span multiple services requires careful consideration</li>
    <li>Deciding when to adopt the microservice architecture is difficult</li>
</ul>


## 1.6 The Microservice Architecture Pattern Language

### 1.6.1 Microservice Architecture is not a Silver Bullet

### 1.6.2 Patterns and Pattern Langauges

### 1.6.3 Overview of the Microservice Architecture Pattern Language

## 1.7 Beyond Microservices: Process and Organization

### 1.7.1 Software Development and Delivery Organization

### 1.7.2 Software Development and Delivery Process

### 1.7.3 The Human Side of Adopting Microservices

## Summary