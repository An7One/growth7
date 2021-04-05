# Chapter 03, Storage and Retrieval
## Section 01, Data Structures That Power Your Database

### Hash Indexes
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