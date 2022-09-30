---
description: >-
  You can find a summary of all new information of every AMA by OriginTrail's
  team here.
---

# Team AMA Summaries



**September 7, 2022: Discord AMA**

* [x] &#x20;The team is working on a **Universal Resolver** for the UALs so that all applications and browsers will be able to understand it
  * This is similar to a **Web3 DNS resolver** and it's completely **in line with GS1 Digital Link standard**

**Bounty Program answers:**

* [x] &#x20;Bounty program will be **live until mainnnet launch**
* [x] &#x20;The telemetry website is constantly updating (both automatically and manually) and data will be available in a couple of days
* [x] &#x20;Bounty pool for Github contributors will be **split based on individual contributions**
* [x] &#x20;Contributors will be able to participate in "**BDD tests**" in the coming days
* [x] &#x20;Bounty for Project Magnify is tied to creating search results, however the quality of results is also an important metric
* [x] &#x20;Project Magnify contributors with the most sought after UALs will benefit most when Magnify goes live

**V6 Mainnet Launch answers:**

* [x] &#x20;**Mainnet Launch is contigent on the v6 testnet performance**
* [x] &#x20;V6 Mainnet is being launched in **3 stages** (currently stage 2):
  * **Stage 1: Prerequisite preparations**
    * **OT Parachain readiness**: Updates and security verification to be completed within the month of September
    * **TRAC availability on OT Parachain**: Teleport Batch #1 is complete and very promising. This condition is met as TRAC gets unlocked on OT Parachain
  * **Stage 2 (current phase): DKG V6 KPI verifications**
    * Optimizing feature KPIs such as network communication speed (affecting publishing and querying) and updating dependencies which should remove some of the remaining vulnerabilities
    * Each release allows the team to test for security and stability of the network and we should expect a couple more releases to reach the required levels of network performance and stability
  * **Stage 3: Network activity**
    * Verification through network usability testing like Project Magnify
    * Project Magnify learnings are crucial inputs into modifications required for transitioning current adoption of OriginTrail from v5 to v6
    * **v5 migration**: Once v6 hits mainnet, **both v5 and v6 networks will be running in parallel** until v5 network fades out due to lack of activity and incentivisation

**V6 node answers:**

* [x] &#x20;Node requirements should be similar as current testnet requirements
  * 4gb RAM, 2 CPU, 50gb
  * The storage required might increase with network activity, therefore **choose a VPS provider that can scale**
* [x] &#x20;There is no change in the stake amount (3k TRAC) planned at the launch of the v6 network
* [x] &#x20;The asset publisher will still be able to set the time period they like, however will be able to also extend the period (by depositing more tokens)
* [x] &#x20;Running local nodes is possible but requires a proper [NAT](https://docs.libp2p.io/concepts/nat/) setup in order to reach the network.
* [x] &#x20;Geolocation of your node is going to have a minimum impact on your node's effectiveness on the network
* [x] &#x20;The amounts of TRAC and OTP required to publish assets will be dynamic based on market conditions

**Project Magnify answers:**

* [x] &#x20;Magnify will support all blockchains that are used by the DKG v6, however starting with OT Parachain
* [x] &#x20;The idea of owning a search result is basically a redefinition of Internet search as we know it today.
* [x] &#x20;The value of each asset/search result will be determined as a function of search frequency and quality (verifiability as well) of information linked to the asset
* [x] &#x20;Ultimately, the asset discovery is expected to result in desirability for these same search results as assets which can be transacted/traded
* [x] &#x20;One of the most significant goals is to provide technical shaping towards best possible UX that would best serve the increased network activity (ie. asset publishing) based on the new asset - based paradigm (and new role of “asset publisher”)
* [x] &#x20;The **light client** is very related to Project Magnify and will receive more iterations past stage 3 of launch

**Possible misuse and manipulations:**

Possible misuse and manipulations are an important topic that are unlikely to have a single-cut solution. Web3 ownership-first approach offers a drastically different way of introducing incentivisation for quality content (e.g. there is little sense in owning a low-quality search result, as this importantly involves a cost at creation of a search result) as well as possibility of open algorithms approach for discoverability (since DKG is a public infrastructure, not a proprietary database). This creates a field of open innovation/competition to create the best approach in weeding out the bad actors.

**August 31, 2022:** [**Project Magnify**](https://projectmagnify.io/create)

* [x] &#x20;Project Magnify is officially in **closed beta** for DKG V6 testnet participants ([bounty program](https://bountyprogram.origintrail.io/) 50k TRAC and 50k OTP)
* [x] &#x20;Participants can now publish assets directly on the **frontend web interface** using test TRAC and test OTP
* [x] &#x20;The team is actively taking questions and helping the community with the Magnify interface on [**Discord**](https://discord.com/channels/460837319025623050/1012026740601786469)
* [x] &#x20;The first iteration of Project Magnify will focus on **helping Web3 users create search results (DKG assets)** and **interacting directly with DKG Nodes and OriginTrail Parachain via the DKG-client (dkg.js)**
* [x] &#x20;DKG v6 is splitting responsibilities between the **clients** and the **node runners**. **You don't need to run a node in order to publish (create assets) anymore** - you can rather connect to the RPC of a node in the network (similar to how blockchains work)
* [ ] &#x20;**Bulk publishing** will be a feature to come later on for NFT creators and such

**August 19, 2022:** [**DKG V6 Testnet Stage 2**](https://bountyprogram.origintrail.io/)

* [x] &#x20;**Increased the amount of TRAC (+added OTP) for bounty program**, totaling 350k TRAC and 50k OTP
* [ ] &#x20;Bounty Program officially confirmed to end when V6 hits mainnet
* [x] &#x20;V6 testnet node runners can now wipe their servers and reinstall a stage 2 node using [these](https://github.com/OriginTrail/dkg-docs/blob/master/decentralized-knowledge-graph-layer-2/testnet-node-setup-instructions/setup-instructions-dockerless.md) instructions.
* [x] &#x20;Mapping EVM and Substrate accounts now available through this [interface](https://parachain.origintrail.io/parachain-account-mapping)

**August 18, 2022:** [**TRAC Teleportation**](https://teleport.origintrail.io/)

* [x] &#x20;**Teleportation Batch #1** (10M TRAC) completely filled up within 1 hour
* [x] &#x20;OTP is now **EVM compatible** and **supports hardware wallets** (Ledger)
* [x] &#x20;Two addresses can be used on OTP, **EVM transactions** (with an Ethereum wallet) and **Substrate transactions** (with Polkadot wallet)
* [ ] &#x20;Teleported TRAC can be used by:
  * **Asset Publishers** to mint their own [**Web3 UALs**](https://twitter.com/\_i\_o\_t\_b/status/1458896467733606410) for search results, native NFTs, social profile and to magnify their search performance
  * **Token Holders** to delegate to DKG nodes, delegate OTP to parachain collators, and provide liquidity to the new native TRAC-OTP AMM Liquidity pool
  * **System runners** to run DKG v6 nodes, run OTP collators, build applications with the DKG and UALs with SDKs
  * **Asset consumers** to search Web3 for verifiable assets - social media posts, art, NFTs and real world assets published on the DKG and purchase UALs and own their linked assets

**August 16, 2022: Twitter Space**

* [ ] &#x20;**DKG Mainnet Launch on September 8, 2022** after the completion of the first TRAC Teleportation Batch
* [ ] &#x20;**DKG BETA Stage 2** and **Magnify Project** begin August 19
* [ ] &#x20;DKG V6 is **enterprise ready** with interest of new enterprises we haven't heard before
