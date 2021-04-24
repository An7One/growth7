# Lecture 3 Google File System

### Section 00

Bio Storage

Why Hard

Performance -> Sharding

Fault -> Tolerant

Tolerance -> Replication

REPL -> In Consistency

Consistent -> Low Performance

### Section 01

Strong Consistency

figure

### Section 02

Bad REPL Design

figure

### Section 03

GFS

Big, fast

Global

Sharding

Automatic recovery

Single data center

Internal Use

Big Sequential Access

### Section 04

figure

Master Data (RAW)

filename -> array of chunk handles(nv)

handle -> list of chunk servers(v), version number(nv), primary(v), lease expiration(v)

log, checkpoint -> Disk

### Section 05

READ

<ol>
    <li>name, off -> M</li>
    <li>M series, list of S; cache</li>
    <li>C -> CS; <- data </li>
</ol>

### Section 06

Writes

No Primary - On master

Find up to Date Replicas

Pick Primary, Secondary: version number

Increments

Tells Primary, Secondary: version number - Lease

Master writes: version number

P picks off all replicas told to write at off





### Reference:

[Youtube](https://youtu.be/EpIgvowZr00) Letcture 3: GFS
