# Chapter 07, Transactions
## The Slippery Concept of a Transaction

### The Meaning of ACID
<ul>
    <li>Atomicity</li>
    <li>Consistency</li>
    <li>Isolation</li>
        <ul>
        <li>in the sense of ACID, means that concurrently executing transactions are isolated from each other: they cannot step on each other's toes.</li>
        <li>the classic database textbooks formalize isolation as <em>serializability</em>, which means that each transaction can pretend that it is the only transaction running on the entire database.</li>
        <li>the database ensures that when the transactions have committed, the result is the same as if they run <em>serially</em> (one after another), even though they may have run concurrently</li>
    </ul>
    <li>Durability</li>
    <ul>
        <li>is the promise that once a transaction has committed successfully, any data it has written will not be forgotten, even if there is a hardware fault or the database crashes.</li>
    </ul>
</ul>

### Single-Object and Multi-Object Operations

#### Single-object writes

#### The need for multi-object transactions

#### Handling errors and aborts
