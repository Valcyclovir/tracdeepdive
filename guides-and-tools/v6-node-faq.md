---
description: This section covers all questions regarding V6 nodes
---

# V6 Node FAQ

### Running a node prior to V6 required 3k TRAC. Why does a V6 node require 50k TRAC ?

There are multiple reasons as to why the initial stake has been revised upwards.&#x20;

{% hint style="info" %}
First and foremost, running a full node now comes with a much greater responsibility both in terms of **persisting the public DKG state** and **providing a high quality of service** to asset publishers.
{% endhint %}

Prior to V5, the model to discourage bad behaviour by Data Holders (node runners) was to collaterize the same amount as the Data Creator for the duration of the job. In other words, the node runner would be punished by completely losing their collateral if they failed a litigation check.&#x20;

{% hint style="success" %}
This V5 model would not require a significant initial stake due to harmful behaviours not related to was punished through losing the collateral to the job, ignoring&#x20;
{% endhint %}



Like many projects out there running a full node has a barrier for entry (like 32 eth to run a node), and there should be more people delegating than people running actual full nodes. The move is a good one too in terms of providing more trust between DC and DH, if anyone with 1k$ can run a node and slashing 5% is merely 50 TRAC, it's not significant enough for nodes to behave properly

Stakes need to be a bit higher so slashing is a deterrent to bad behaviour



As stake slashing needs to be a meaningful deterrent to potential service outages, given the proposed slashing implementation above, the minimum required amount of posted stake for a full node will be increased to 50 000 TRAC in order to be eligible for operation



#### **What Is Slashing?**

Most Proof-of-Stake blockchains have **reward and penalty mechanisms**. Good behaviors are encouraged through rewards. Validators receive rewards for both attesting and proposing blocks to the blockchain as a percentage of their stake.

On the flip side, bad behaviors, inactivity, and dishonest validations are subject to a penalty called slashing. This mechanism is designed to discourage malicious validator behavior and to incentivize network participation, as well as node security and availability.

The particularities of slashing vary from one protocol to another and are defined within them. In many cases, a predefined percentage or a fixed amount of a validator’s stake is lost if it doesn’t behave as expected. Some protocols even apply a complete slashing of the stake or remove the validator from the group either for the current epoch or permanently.

To incentivize security and decentralization, some networks, such as **Polkadot** and ETH2, use the so-called correlated slashing. This means that the penalty escalates based on the percentage of total validators that engage in the bad behavior at the same time. Let’s say that 10 out of 100 validators are down. In such a case, the slashing penalty is smaller per validator than if 25 out of 100 validators are down.



#### **Conclusion for Slashing**

Slashing is a mechanism used by PoS protocols to discourage harmful behaviors and make validators more responsible. They help keep the network secure since, without slashing penalties, a validator can use the same node to validate blocks on multiple chains or do so on the wrong chain. PoS protocols that don’t have slashing penalties are considered less secure.
