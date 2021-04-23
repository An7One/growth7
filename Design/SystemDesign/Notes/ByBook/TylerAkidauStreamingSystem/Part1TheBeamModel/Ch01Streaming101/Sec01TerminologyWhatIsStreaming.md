# Chapter 01 Streaming 101

## Terminology: What is Streaming?

2 important and <i>orthogaonal</i> dimensions:

<ol>
    <li>Cardinality</li>
    <ul>
        <li>Bounded Data</li>
        <li>Unbounded Data</li>
    </ul>
    <li>Constitution</li>
    <ul>
        <li>Table</li>
        <li>Stream</li>
    </ul>
</ol>

### On the Greatly Exaggerated Limitations of Streaming

Lambda Architecture, the basic idea is that one runs a streaming system alongside a batch system, both performing essentially the same calculation.

[O'Reilly Post](https://www.oreilly.com/radar/questioning-the-lambda-architecture/) - Jay Kreps - Questioning the Lambda Architecture

2 things:
<ol>
    <li>Correctness</li>
    <ul>
        <li>At the core, correctness boils down to consistent storage</li>
        <li><a href="https://www.oreilly.com/content/why-local-state-is-a-fundamental-primitive-in-stream-processing/#:~:text=There%20are%20three%20primary%20reasons,access%20is%20easier%20to%20isolate">O'Reilly Post</a> - Jay Kreps - Why is local state a fundamental primitive in stream processing?</li>
    </ul>
    <li>Tools for Reasoning about Time</li>
</ol>

### Event Time v.s. Processing Time

2 domains of time of interests:

<ol>
    <li>Event Time</li>
    <li>Processing Time</li>
</ol>