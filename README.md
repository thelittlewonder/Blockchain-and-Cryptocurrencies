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

## Zero-Knowledge Proof
In cryptography, a zero-knowledge proof is a method by which one party can prove to another party that it knows a value x, without conveying any information apart from the fact that it knows the value x. 

If proving the statement requires knowledge of some secret information on the part of the prover, the definition implies that the verifier will not be able to prove the statement in turn to anyone else, since the verifier does not possess the secret information.
[Example](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/)

## ECDSA
Elliptic Curve Digital Signature Algorithm or ECDSA is a cryptographic algorithm used by Bitcoin to ensure that funds can only be spent by their rightful owners.

## ECDLP
Elliptic Curve Discrete Logarathmic Problem: g^r%p=x. Given x,g and p find r.

## Gas
When you send tokens, interact with a contract, send ETH, or do anything else on the blockchain, you must pay for that computation. That payment is calculated in Gas and gas is paid in ETH.

You are paying for the computation, regardless of whether your transaction succeeds or fails. Even if it fails, the miners must validate and execute your transaction (compute) and therefore you must pay for that computation just like you would pay for a successful transaction.

## Private Blockchain
A Private Blockchain  Network requires an invitation to participate in the  network. The invitation must be validated either by network starter or by the rules/conditions placed by the network starter.

Permissioned Blockhain Network puts restriction to the entry of participant and allows only the kind of participant that is required in the network. Any entity willing to participate must be invited or obtain a permission to join the network. Once the entity has joined the network, it can start the activity of maintaining the Private Blockchain Network in a decentralized manner.

- Existing participants can decide the entry of new participants
- A regulatory authority can be set up which can issue licenses for participation
- A consortium can be formed to make the decision of entry of future participants
- Or any other way that the network founders may think fit.


#### Advantages
- Increased privacy
- Enviornment-friendly as less computational power is required to achieve the consensus.(as in the case of Public Network)

#### Disadvantages
- Less secured as compared to public network

## Public Blockchain Network
A public Blockchain network or permissionless Blockchain network is completely open-ended and anyone willing to participate in this kind of network can participate without any permission. This is the major and only difference between public and private Blockchain network

Anyone can participate in the permissionless network, execute the consensus protocol and maintain the shared open public ledger.

Public Blockchain network has a system of providing incentives to the participants, which encourages entities to participate.More the number of participants, more is the security and accuracy of the transaction.

### Advanatges
- More secured as compared to Private Network

### Disadvanatges
- Low privacy
- Huge computational power and energy is required, less eco-friendly.

## Nakamoto Consensus
- Consensus Algorithm of Bitcoin.
- The consensus protocol says that the **first announced valid block containing solution to a computational puzzle is considered correct**; and all other miners are to start searching for a followup block after that moment. 
- This may occasionally lead to temporary forks due to several simultaneously found solutions. **The longest fork in that case is considered valid**. In case of equal-length forks miners can choose either one. Due to probabilistic nature of computational puzzle, one fork will eventually get longer than the other.

## Proof of Stake
- POW requires Electricity and Centralisation may occur (Mining Pools).
- In POS, Validators Chosen randomly on basis of their stake.
- In order to validate transactions and create blocks, a forger must first put their own coins at ‘stake’
- Validators loose their stake if they approve fraud transaction. If accepted, you gain.
- 51% attack - less likely since 51% of total currency is very large money.

## Proof of Burn
- The way proof of burn works is that **miners send coins to an unspendable address** (also known as an eater address), effectively burning them.
- The idea behind proof of burn is that by **burning a cryptocurrency, a user is demonstrating a willingness to undergo a short-term loss for a more long-term investment.**
- Users are rewarded over time through the proof of burn reward mechanism when mining, earning a lifetime privilege to mine on the system.

## Sybil Attack
- A Sybil attack is an attack where a **single adversary is controlling multiple nodes on a network.** 
- It is **unknown to the network that the nodes are controlled by the same** adversarial entity. 
- Sybil attacks are **avoided in Bitcoin** through the **proof-of-work** mechanism.

## Hash-cash 
It is a proof-of-work algorithm that requires a selectable amount of work to compute, but the proof can be verified efficiently.

## Distributed Ledger
- A distributed ledger is a **database held and updated independently by each participant (or node) in a large network.**
- The distribution is unique: records are not communicated to various nodes by a central authority, but are instead **independently constructed and held by every node.**
- That is, **every single node on the network processes every transaction, coming to its own conclusions and then voting on those conclusions** to make certain the majority agree with the conclusions.
- Once there is this **consensus, the distributed ledger has been updated,** and all nodes maintain their own identical copy of the ledger. This architecture allows for a new dexterity as a system of record that goes beyond being a simple database.

## Soft and Hard Fork
- Hard forks is a permanent divergence in the the block chain, commonly occurs when non-upgraded nodes can’t validate blocks created by upgraded nodes that follow newer consensus rules.

- Soft forks is a temporary divergence in the block chain caused by non-upgraded nodes not following new consensus rules

## The DAO
- Smart Contract: Immutable, Perpetual on a Runtime Environment. Will do whatever it is bound to, no need of interference from other party.
- DAO : Decentralised Autonomous Organisation. Decentralised Kickstarter.
- Receive DAO Tokens for sending ether which could be used for voting on the ideas.
- As a result of the dispute, the network split in two. Ethereum (the subject of this article) continued on the forked blockchain, while Ethereum Classic continued on the original blockchain.

## GHOST
- The Ghost protocol in Ethereum is **(Greedy Heaviest Observed Subtree)**.
- A way of **combating the way that fast block time blockchains suffer from a high number of stale blocks** - i.e. blocks that were propagated to the network and verified by some nodes as being correct but eventually being cast off as a longer chain achieved dominance, or Forking. 
- The protocol also **combats the issue of centralisation bias** – the larger the pool the less time the more often they are going to get a head start on other miners by producing the block themselves and immediately start the race for the next block.
- GHOST **includes stale blocks** – or Uncles as Ethereum calls them – these are included **in the calculation of which chain has the highest cumulative difficulty**. Centralisation is solved by giving **block rewards to stales of 87.5%**
- The **nephew** (child of the Uncle block) also **receives a reward of 12.5%** of the block reward.

## Sidechain
- Sidechains are emerging mechanisms that **allow tokens and other digital assets from one blockchain to be securely used in a separate blockchain** and then be moved back to the original blockchain if needed.
- A sidechain is a **separate blockchain that is attached to its parent blockchain using a two-way peg**.
- The **two-way peg enables interchangeability of assets at a predetermined rate between the parent blockchain and the sidechain**.

## Namecoin
- based on the code of bitcoin and uses the same proof-of-work algorithm.
- Namecoin can **store data within its own blockchain transaction database** and acts as **decentralised domain name system**
- Namecoin's flagship use case is the **censorship-resistant top level domain .bit**, which is functionally similar to .com or .net domains but is **independent of ICANN, the main governing body for domain names**.


## Bloom Filter
- A Bloom filter is a **data structure** designed to tell you, **rapidly and memory-efficiently**, whether **an element is present in a set**.
-  Bloom filter is a **probabilistic data structure:** it tells us that the element **either definitely is not in the set** or **may be in the set.**

### How it works
Each **empty cell in that table represents a bit**, and the **number below it its index.** To **add an element** to the Bloom filter, we simply **hash it a few times** and **set the bits in the bit vector** at the index of those hashes to 1.

### Testing Membership
To **test for membership**, you simply **hash the string** with the same hash functions, then **see if those values are set in the bit vector.** If they aren't, you know that the element isn't in the set. If they are, you only know that it might be, because another element or some combination of other elements could have set the same bits. 

### Other Points
- The hash functions used in a Bloom filter should be **independent** and **uniformly distributed**. They should also be as **fast** as possible (cryptographic hashes such as **sha1**, though widely used therefore are **not very good choices**).

## Proof of Elapsed Time
- Used by Sawtooth Hyperledger
- **Each participant** in the blockchain network **waits a random amount of time.**
- The **first** participant to **finish waiting** gets to be **leader for the new block.**
- Requirements : First, did the lottery **winner actually choose a random** wait time? Second, did the lottery **winner actually finish waiting** the specified amount of time?
- Depends on **Intel Software Guard Extensions (SGX)** which allows **applications to run trusted code in a protected environment.**
- For PoET, the trusted code is what ensures that these **two requirements are satisfied** — keeping the lottery fair.

## Ethash
- Ethash is the planned PoW algorithm for Ethereum 1.0.
- Memory Hard : 
	- **Every mixing** operation requires a **128 byte read from the DAG** .  **Hashing a single nonce requires 64 mixes**, resulting in (128 Bytes x 64) = 8 KB of memory read
	- The **reads are random access** , so **putting a small chunk of the DAG in an L1 or L2 cache isn’t going to help** much, since the next DAG fetch will very likely yield a cache miss.
![a](https://vijaypradeep.com/static/media/uploads/ethash_algorithm.png)

## Merkel Tree
![merkletree](https://cdn-images-1.medium.com/max/1600/1*TANA9WXlfDz3FNoNfrSGVw.png)

## Simple Payment Verification
- A method for **verifying if particular transactions are included** in a block **without downloading the entire block.**
-  A user only needs to keep a **copy of the block headers of the longest proof-of-work chain** and **obtain the Merkle branch linking the transaction to the block it's timestamped in.**

## Full Node
- A full archive node synchronizes the blockchain by **downloading the full chain, from the genesis block to the current head block, executing all of the transactions contained within**. 
- Typically, **miners store the full archive node**, because they are required to do so for the mining process.

## Light Node
- Instead of downloading and storing the full chain and executing all of the transactions, **light nodes download only the chain of headers, from the genesis block to the current head, without executing any transactions or retrieving any associated state**.
