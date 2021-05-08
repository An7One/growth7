# Chapter 03 Storage and Retrieval

## Section 01 Data Structures That Power Your Database

### Hash Indexes

Compaction means throwing away duplicate keys in the log, and keeping only the most recent update for each key.

Moreoever, since compaction often makes segments much smaller, one can also merge several segments together at the same time as performing the compaction.

#### Issues important in real implementations

<ul>
    <li>File format</li>
    <li>Deleting records</li>
    <li>Crash recovery</li>
    <li>Partially written records</li>
    <li>Concurrency control</li>
</ul>

### SSTables and LSM-Trees

#### Constructing and maintaining SSTables

#### Making an LSM-tree out of SSTables

#### Performance optimizations

Bloom filter, a memory-efficient data structure for approximating the contents of a set.

### B-Trees

#### Making B-trees reliable

#### B-tree optimizations

### Comparing B-Trees and LSM-Trees

#### Advantages of LSM-trees

#### Downsides of LSM-trees

### Other Indexing Structures

#### Storing values within the index

#### Multi-column indexes

#### Full-text search and fuzzy indexes

#### Keeping everything in memory
