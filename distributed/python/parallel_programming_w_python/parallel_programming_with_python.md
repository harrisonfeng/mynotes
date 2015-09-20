# Parallel Programming with Python

Parallel programming can be defined as a model that aims to create programs 
that compatible with environments prepared to execute code instructions 
simultaneously.

`pseudo-parallelism` based on `time-slicing`, from Intel 80386 in \'80s, which 
means to allow the execution of tasks in a `pre-emptive` manner, that is,
it was possible to periodically interrupt the execution of a program to 
provide processor time to another program.


`pipelining` system, from Intel 80486 in the late \'80s, which in practice,
divided the stage of execution into distinct substage. In practical terms,
in a cycle of the processor, we could have different instructions being 
carried out simultaneously in each substage.


`mult-core`


## Why use paralle programming?

## The common forms of parallelization

`Concurrent programming is an abstruction from parallel progamming. Concurrent
 systems dispute over the same CPU to run tasks.

 Parallel programming can be defined as an approach in which program data 
 creates workers to run specific tasks simultaneously in a multicore 
 environment without the need for concurrency amongst them to access a CPU.

 Parallel systems run tasks simultaneously.

 Distributed programming aims at the possibility of sharing the processing 
 by exchanging data through messages between machines (nodes) of computing,
 which are physically separated.

 Distributed programming is becoming more and more popular for many reasons;
 They are expected as follows:
 
 * Fault-tolerance
 * Horizontal scalability
 * Cloud computing

 Distributed systems run tasks within physically-separated nodes.

 ## Communicating in parallel programming

 In most cases,the communication in parallel systems is established in such 
 way that data can be exchanged amongst workers. There are two forms of 
 communication that are more widely known:

 * shared state
 * message passing

### Understanding the shared state

