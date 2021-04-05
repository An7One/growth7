# Cache
## Redis

### Eviction Policy
<ol>
    <li>No eviction</li>
    <li>All keys LRU</li>
    <li>Volatile LRU</li>
    <li>All keys random</li>
    <li>Volatile random</li>
    <li>Volatile TTL</li>
</ol>

### Persistence
<ol>
    <li>RDB snapshot</li>
    <ul>
        <li>a point-in-time snapshot of all one's dataset</li>
        <li>stored in a file in disk and performed at specific intervals</li>
        <li>this way, the dataset can be restored on startup</li>
    </ul>
    <li>AOF log</li>
    <ul>
        <li>an append-only file log of all the write commands performed in the Redis server</li>
        <li>stored in disk</li>
        <li>by re-running all the commands in their order, a dataset can be restored on startup</li>
    </ul>
</ol>

## Resource
[简书](https://www.jianshu.com/p/929bc7ee8063) - Redis的优缺点