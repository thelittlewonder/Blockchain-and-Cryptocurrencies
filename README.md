# IBCC630C

## Distributed Database: 
A distributed database is a database in which **storage devices are not all attached to a common processor**. It may be stored in multiple computers, located in the same physical location; or may be dispersed over a network of interconnected computers.

- Homogenous: Same Hardware and Software
- Heterogenous: Different Hardware

Two processes ensure that the distributed databases remain up-to-date and current: replication and duplication.

- Replication involves using specialised software that **looks for changes in the distributive database**. Once the changes have been identified, the replication process makes all the databases look the same. The replication process can be complex and time-consuming depending on the size and number of the distributed databases. This process can also require a lot of time and computer resources.
- Duplication, on the other hand, has less complexity. It basically **identifies one database as a master and then duplicates that database.** The duplication process is normally done at **a set time** after hours. This is to ensure that **each distributed location has the same data**. In the duplication process, **users may change only the master database**. This ensures that local data will not be overwritten.

![](https://cdn-images-1.medium.com/max/1600/1*6QfLE7nibZs2ulAdLOkMvw.jpeg)

## Proof of Work:
A proof-of-work (PoW) system is an economic measure to **deter denial of service attacks and other service abuses** such as spam on a network **by requiring some work from the service requester**, usually meaning processing time by a computer.  Verification however is easy.

**51% attack** - Results in double spending. I can make a private chain since I have highest hashing power and at the same time spend from the public chain. Then later I will announce private chain in public and network will accept it since it is the longest. [Source](https://www.youtube.com/watch?v=UxyGt58EPa4) 

## Byzantine Problem
Imagine that the grand Eastern Roman empire aka Byzantine empire has decided to capture a city. Alas, there is fierce resistance from within the city. The Byzantine army has completely encircled the city. The army has many divisions and each division has a general. The generals communicate between each as well as between all lieutenants within their division only through messengers.

All the generals or commanders have to agree upon one of the two plans of action. Exact time to attack all at once or if faced by fierce resistance then the time to retreat all at once. The army cannot hold on forever. If the attack or retreat is without full strength then it means only one thing — Unacceptable brutal defeat.

If all generals and/or messengers were trustworthy then it is a very simple solution. However, some of the messengers and even a few generals/commanders are traitors. They are spies or even enemy soldiers. There is a very high chance that they will not follow orders or pass on the incorrect message. The level of trust in the army is very less.

![](https://cdn-images-1.medium.com/max/1600/1*1vFslrPsES7z62QuaeTP4g.jpeg)

### Solution
**Number of generals should be greater than three times the number of traitors**
#### - Majority Consideration
#### - Signature(Primary and Public Key):
The difficulty of BGP is in the ability of a traitor lieutenant to lie about the commander's order. If we can restrict this ability by making the following assumptions, BGP is solvable with any number of traitors as long as their maximum number is known.

In addition to the 3 assumptions made in the solution with oral messages, we add the following assumption.
- A loyal general's signature cannot be forged, any alteration can be detected. -> can drop a message, but can't change it
- Any one can verify the authenticity of a signature. -> no one can fool a general

The solution:

- the commander sends a signed order to lieutenants
- if a lieutenant receives an order from some one (either from commander directly, or from other lieutenants), he verifies it and then puts it in a set V if it's not already there. Relay the order if there are less than m distinct signatures on the order.
- Everyone halts at round m+2, and use choice(V) as the desired action
#### - Broadcast and CRC

## Two Generals Problem
Two armies, each led by a different general, are preparing to attack a fortified city. The armies are encamped near the city, each in its own valley. A third valley separates the two hills, and the only way for the two generals to communicate is by sending messengers through the valley. Unfortunately, the valley is occupied by the city's defenders and there's a chance that any given messenger sent through the valley will be captured.

The problem is to come up with algorithms that the generals can use, including sending messages and processing received messages, that can allow them to correctly conclude:
**Yes, we will both attack at the agreed-upon time.**

## Memory Hard
It refers to a situation in which the time to complete a given computational problem is decided primarily by the amount of memory required to hold data. The application of memory hard functions could prove to be valuable in preventing spam, which has become a problem of epidemic proportions on the Internet.

##  Hadoop Distributed File System
Hadoop File System was developed using distributed file system design. It is run on commodity hardware. Unlike other distributed systems, HDFS is **highly faulttolerant and designed using low-cost hardware**.

To store such huge data, the files are stored across **multiple machines**. These files are **stored in redundant fashion to rescue the system from possible data losses in case of failure.**
[Video](https://www.youtube.com/watch?v=1_ly9dZnmWc)

Problems
- Updation of data.
- Regular ping machines to check if alive.

## Distributed Hash Table
![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/98/DHT_en.svg/1000px-DHT_en.svg.png)
A distributed hash table (DHT) is a class of a decentralized distributed system that provides a lookup service similar to a hash table: (key, value) pairs are stored in a DHT, and any participating node can efficiently retrieve the value associated with a given key.

**Problem: Recalculate hash after updation of node**

### Consistent Hashing:
Consistent hashing is a special kind of hashing such that when a hash table is resized, only K/n keys need to be remapped on average, where K is the number of keys, and n is the number of slots. In contrast, in most traditional hash tables, a change in the number of array slots causes nearly all keys to be remapped because the mapping between the keys and the slots is defined by a modular operation.

### Rendezvous Hashing:
Rendezvous hashing (aka Highest Random Weight hashing) is an algorithm to achieve distributed agreement on a set of k options out of a possible set of n options. It's most typically used in distributed systems to find out the location of some resource.

## ASIC Resistance
ASIC stands for Application-specific integrated circuit. An ASIC is another way of running a program or calculation or what have you (in our case mining) using a PCB/Hardware instead of Software running on a general purpose computer. GPUs are technically ASICs, their application being graphics processing and output.

ASIC resistance means that there will be no significant speedup by implementing the algorithm in an ASIC, as compared to a CPU based implementation.

This is usually achieved by requiring a lot of memory, which when implementing this on an ASIC, translates to needing lots of physical area on the chip.

ASIC implementations derive their power from having many physically parallel and pipelined threads on one chip, each requiring a certain piece of chip real estate. Now if your algorithm requires lots of real estate even for one step of the pipeline, there will not but much room to actually parallelize or pipeline the algorithm. Thereby you will lose the parallelizing advantage of an ASIC implementation.

## Turing Complete
Turing-completeness refers to any device or system which in theory can calculate everything assuming enough memory is available. And since software is just programmed, and programming is just chaining mathematic statements, everything can be implemented in a turing complete environment.

## Hashing Algorithm
- Pre-Image Resistance : Given h, we can't produce a x such that H(x)=h.
- Second Pre-Image Resistance: For a given message x1, it is hard to find a second message x2≠x1 with H(x1)=H(x2)
- Collision Resistance: It is hard to find a pair of messages x1≠x2 with H(x1)=H(x2).
