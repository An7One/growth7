
# Chapter 05, Replication
## Summary

Replication can serve several purposes:
<ul>
    <li>High availability</li>
    <ul><li>to keep the system running, even when one or several mathines, or an entire datacenter goes down</li></ul>
    <li>Disconnected operation</li>
    <ul><li>to allow an application to continue working when there is a network interruption</li></ul>
    <li>Latency</li>
    <ul><li>to place data geographically close to uses, so that users can interact with it faster</li></ul> 
    <li>Scalability</li>
    <ul><li>to be able to handle a higher volume of reads than a single machine could handle, by performing reads on replicas</li></ul>
</ul>