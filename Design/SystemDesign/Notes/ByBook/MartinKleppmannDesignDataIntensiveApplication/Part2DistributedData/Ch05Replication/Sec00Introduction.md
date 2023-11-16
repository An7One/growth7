# Chapter 05, Replication

## Introduction

There are various reasons why one might want to distribute a data across multiple mathines:

- Scalability
  - if the data volume, read load, or write load grows bigger than a single machine can handle, one can potentially spread the laod across multiple machines.
- Fault Tolerance/High Availability
  - when one machine fails, another one can take over.
- Latency
  - users at various locations worldwide can be served from datacenters geographically close to them.
