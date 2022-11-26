# September 2022

### **September 7, 2022: Discord AMA**

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
