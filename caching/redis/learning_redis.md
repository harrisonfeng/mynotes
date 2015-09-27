# Learning Redis

## Introduction to NoSQL

Not only SQL or NoSQL

ACID properties represent the consistency and availability of the CAP theorem.
These properties are exhibited by RDBMS and stand for the following:

* **Atomicity**: In a transaction, all operations will complete or none will be
completed (rollback)
* **Consistency**: The database will be in a consistent state during the start 
and end of a transaction and cannot leave the state in between.
* **Isolation**: There will be no interference among the concurrent transactions.
* **Durability**: Once a transaction commits, it will remain so even after the 
server restarts or fails.

**BASE** properties are exhibited by NoSQL; then represent the availability
and partition tolerance of the CAP theorem. They basically give up on the 
strong consistency shown by RDBMS. BASE stands for following features:

* **Basically availabile**: This guarantees a response to a request even if 
the data is in the stale state.
* **Soft state: The state of the data is always in position to accept change 
even when there is no request to change its state. What this means is that 
suppose there are two nodes holding the same of a data (the replication of 
data), if there is a request to change the state in one of the nodes, the 
state in the other node will not change during the lifespan of the request.
The data in the other node will change its state due to asynchronous process 
triggered by the datastore, thus making the state soft.
* Eventually consistent: Due to the distributed nature of the nodes, the system 
will eventually become consistent.

> The data writes and reads should be faster and easier.

The categories in NoSQL that emerged based on different data models are as 
follows:

* Graph-oriented NoSQL
* Documentation-oriented NoSQL
* Key-value oriented NoSQL
* Column-oriented NoSQL

### Graph-oriented NoSQL

A graph structure consists of a node, edges and properties. The way to understand 
graph databases is to think of them as mindmaps with bidirectional relationships.
What this means is that A is related to B and B is related to C, then C is related 
A. Graph databases tend to solve the problems that arise out of relationships formed
among unstructured entities at runtime, which can be bidirectional.

### Column-oriented NoSQL

Cassandra is a datastore which belongs to the category of columnar-oriented datastores 
and also shows some features of the key-value datastore. Cassandra, which was initially 
started by Facebook but later forked to the Apache open source community, is best suited 
for real-time transaction processing and real-time analytics.


