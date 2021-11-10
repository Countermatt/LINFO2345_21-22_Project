# LINFO2345 Project : Proof of Stack Blockchain

**2021** -- *Matthieu Pigaglio and Peter Van Roy*


**The objective of this project is the implementation of a Blockchain using Proof of Stake (PoW) in Erlang**

*This project is composed of 3 parts*

- *Deploy a network of Erlang process,*
- *Implement and deploy a consensus algorithm for the Proof of Stake,*
- *Implement and deploy the blockchain algorithm using the consensus algorithm to create new block.*

## Context

A blockchain is a **decentralized list of record** which use cryptography to guarantee the integrity of all record store in it. A blockchain is composed of several list of record named **blocks**. Each blocks is constructed using the previous blocks to guarantee all the transaction stored in it. To construct a block, each peer of the system attempt to resolve a **cryptographic puzzle** to create the new block by **brute force**. The first node which resolve the puzzle push the new block in the blockchain and communicate it to other peers.
This method to construct a blockchain is the **Proof of Work** (PoW).

The PoW have some disadvantage to create blocks:
- If an attacker want to modify a record in a block, he need to recalculated all the successor block. But during this time, the honest nodes continue to create blocks. So, an attacker need a to big amount of ressources to recreate all blocks faster than the honest node.
- The creation of block by brute force use a huge amount of ressources (CPU/GPU power, electricity, ...). Today, Bitcoin use an amount of electricity equal to the consumption of Hungary.

To solve the problem of PoW, we create the **Proof of Stake** (PoS) with use a elected group to decide which block to add instead of using a challenge. The creation of the consensus group is pondered by the proportion of the blockchain crypto currency a node owned. The more of it a node owned the more chances he have to be in the consensus group. Because a node which have a lot of currency don't want the blockchain to collapse so he will take decision in the interest of the blockchain.


## The Project

Your task is composed of 3 parts:

- Deploy a network of connected peers,
- Implement and deploy an election and consensus algorithm for the Proof of Work,
- Implement and deploy a blockchain using the consensus algorithm to add new block


## Network deployment

This part of the project consist in the implementation and the deployment of network of connected node which will be use for the blockchain.

All the node of the system need to be connected to all others node to communicate for the consensus, send blocks to the consensus group and receive the validated block from the consensus group.


## Consensus Group Implementation
