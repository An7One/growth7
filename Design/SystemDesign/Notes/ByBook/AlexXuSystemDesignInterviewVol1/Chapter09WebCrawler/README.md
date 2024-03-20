# Chapter 09: Design a Web Crawler

A crawler is used for many purposes:

- Search engine indexing
- Web archiving
- Web mining
- Web monitoring

## Step 1 - Understand the Problem and Establish Design Scope

### Basic Algorithm

1. Given a set of URLs, to download all web pages addressed by the URLs
2. to extract URLs from these web pages
3. to add new URLs to the list of URLs to download
4. to repeat the above 3 steps

### Functional Requirement

TODO

### Non-functional Requirement

- Scalability
- Robustness
- Politeness
- Extensibility

### Estimation

- QPS - TODO
- Storage - TODO
- TODO

## Step 2 - Propose High-level Design and Get Buy-In

TODO graph

Main component

- Seed URLs
- URL Frontier
- HTML Downloader
- DNS Resolver
- Content Parser
- Content Seen?
- Content Storage
  - most of the content is stored on disk because the data set is too big to fit in memory
  - popular content is kept in memory to reduce latency
- URL Extractor
- URL Filter
- URL Seen?
- URL Storage

### Web Crawler Workflow

TODO graph

## Step 3 - Design Deep Dive

Component and technique to cover:

- Depth-first Search (DFS) and Breadth-first Search (BFS)
  - TODO
- URL Frontier, a data structure that stores URLs to download
  - politness
  - priority
  - freshness
  - storage for URL frontier
- HTML Downloader
  - Robots.txt
  - Performance Optimization
    - distributed crawl
    - cache DNS resolver
    - locality
    - short timeout
- Robustness
  - consistent hashing
  - save crawl states and data
  - exception handling
  - data validation
- Extensibility
- Detect and Avoid Problematic Content
  - redudant content
  - spider traps
  - data noise

## Step 4 - Wrap Up

TODO
