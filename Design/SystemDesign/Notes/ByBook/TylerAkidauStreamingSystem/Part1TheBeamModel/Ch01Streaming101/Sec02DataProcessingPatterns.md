# Chapter 01 Streaming 101

## Section 02 Data Processing Patterns

### Bounded Data

MapReduce

### Unbounded Data: Batch

<ul>
    <li>Fixed Windows</li>
    <ul>
        <li>THe most common way to process an unbounded dataset using repeated runs of a batch engine is by windowing the input data into fixed-size windows and then processing each of those windows as a separate, bounded data source (sometims also called <i>tumbling windows</i>)</li>
    </ul>
    <li>Sessions</li>
    <ul>
        <li>Sessions are typically defined as periods of activity terminated by a gap of inactivity</li>
    </ul>
</ul>

### Unbounded Data: Streaming

#### Time-agnostic

##### Filtering

##### Inner Joins

##### Approximation Algorithms

##### Windowing

<ul>
    <li>Fixed Windows (aka tumbling windows)</li>
    <li>Sliding WIndows (aka hopping windows)</li>
    <li>Sessions</li>
</ul>

##### Windowing by Processing Time

##### Windowing by Event Time

<ul>
    <li>Buffering</li>
    <li>Completeness</li>
</ul>