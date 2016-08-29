---
layout: post
title: Understanding I/O
author: Nilesh Sharma
---

Many times you guys have heard about I/O in terms of programming like for example
Node.js works on the single threaded non blocking I/O model.

So Let's have a look, what is this I/O ?

## Understanding I/O
-----
In computing terms I/O means input/output.

Basically it is the communication between information processing system(Computer in our case) and human.

The definition of Input/Output are: Signals or Data received/sent by system.

When you read somewhere "perform I/O", It simply means to perform and input/output operation.


In terms of computer architecture I/O is the tranfer of information to and from the CPU/Memory Combination.
For example: reading data from disk drive can be considered as Input/Output.

## Types oF I/O
-----
IO can be classified in two types: Blocking(Synchronous) IO and Non-Blocking(Asynchronous) IO.
Let's try to understand all these terms one by one:

**Synchronous vs Asynchronous**:

Synchronous execution: refers to code executing in sequence.
Asynchronous execution: refers to execution that doesn't run in the sequence it appears in the code. 

**Blocking vs Non-blocking**:
Blocking refers to operations that block further execution until that operation finishes.
Non-blocking refers to code that doesn't block execution.


## Advantages of Non-blocking Asynchronous IO:
-----

One advantage of non-blocking, asynchronous operations is that you can maximize the usage of a single CPU as well as memory.

Synchronous, blocking example:
A good example of Synchronous, blocking operations is web servers build in Java or Python handles IO or
network requests.

If your code is reading data from file or database, it'l block everything after it from executing.
In that period our machine is simply holding onto memory and processing time for thread that is not
doing anything.

So for performing other requests while that thread is stalled, mostly softwares spawn threads for additional
requests like for example: Generally we run Python-Django server using uwsgi/nginx which spawns more threads accordingly. This requires more memory consumed and more processing.

Asynchronous, non-blocking example:

Asynchronous, non-blocking servers like ones ones made in Node, only use one thread to service all requests.This means an instance of Node makes the most out of a single thread. The creators designed it with the premise that the I/O and network operations are the bottleneck.

When requests arrive at the server, they are serviced one at a time. However, when the code serviced needs to query the DB for example, it sends the callback to a second queue and the main thread will continue running (it doesn't wait).

Now when the DB operation completes and returns, the corresponding callback pulled out of the second queue and queued in a third queue where they are pending execution. When the engine gets a chance to execute something else (like when the execution stack is emptied), it picks up a callback from the third queue and executes it.

