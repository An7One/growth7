# Chapter 05, Replication
## Introduction
There are various reasons why one might want to distribute a data across multiple mathines:
<ul>
    <li>Scalability</li>
    <ul>
        <li>if the data volume, read load, or write load grows bigger than a single machine can handle, one can potentially spread the laod across multiple machines.</li>
    </ul>
    <li>Fault Tolerance/High Availability</li>
    <ul>
        <li>When one machine fails, another one can take over.</li>
    </ul>
    <li>Latency</li>
    <ul>
        <li>Users at various locations worldwide can be served from datacenters geographically close to them.</li>
    </ul>
</ul>

