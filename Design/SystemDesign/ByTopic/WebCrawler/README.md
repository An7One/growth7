# Web Crawler

## Use Case

- Search Engine Indexing
- Web Archiving
- Web Monitoring
- Web Mining

## Step 1 - Understand the Problem and Establish Design Scope

### Functional Requirement

TODO

### Non-functional Requirement

- Scalability
- Robustness
- Politeness
- Extensibility

### Estimation

TODO

### Schema

TODO

#### Database

#### JSON

#### API

## Step 2 - Propose High-level Design and Get Buy-in

TODO - graph, with the flow

### Seed URLs

A good seed URL serves as a good starting point that a crawler can utilize to traverse as many links as possible.

Based on:

- locality
- topic

### URL Frontier

Most modern web crawlers split the crawl state into two:

- to be downloaded
- already downloaded

One can refer to this as First-in-First-out (FIFO) queue.

### HTML Downloader

To download the web pages from the Internet

### DNS Resolver

To translate URLs into their IP addresses

### Content Parser

TODO

### Content Seen?

TODO

### Content Storage

TODO

### URL Extractor

To parse and extract links from HTML pages.

### URL Filter

To exclude certain content types, file extensions, error links and URLs blacklisted.

### URL Seen?

To keep track of URLs that are visited before or already in the _Frontier_.

Bloom filter and hash table are common techniques to implement _URL Seen?_ component.

### URL Storage

To store already visited URLs.

### Web Crawler Workflow

## Step 3 - Design Deep Dive

TODO

## Step 4 - Wrap Up

TODO

### DFS vs BFS

TODO

### URL Frontier Deep Dive

#### Politeness

#### Priority

#### Freshness

#### Storage for URL Fronter

### HTML Downloader Deep Dive

TODO

## Reference

Web Crawler System Design - [EnjoyAlgorithms](https://www.enjoyalgorithms.com/blog/web-crawler/)

Chapter 09: Design a Web Crawler, System Design Interview, volume1, edition2, by Alex Xu
