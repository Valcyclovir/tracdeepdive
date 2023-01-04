---
description: This is an elaborate Guide and FAQ covering everything related to Teleporting
---

# Teleportation Guide

## Instructions

#### **1. Teleport your TRAC**&#x20;

First, consult the **** [**FAQ** ](trac-teleportation-faq.md#faq)section below to learn about Teleporting TRAC.&#x20;

Once you are ready, teleport your TRAC by visiting [**this**](https://teleport.origintrail.io/) **** website. Make sure you read the steps thoroughly. You must complete the KYC to receive OTP bounty. Once you complete the 2 teleport transactions, your TRAC will leave your wallet and be locked on the smart contract until further notice.

#### **2. Collect OTP bounty**

Visit [**this**](https://teleport.origintrail.io/teleport-reward-claim) website to collect your OTP bounty for teleporting. Make sure you use the same EVM (Ethereum) wallet you used to teleport TRAC on step 1. Then, paste a self-custody substrate (Polkadot) wallet of your choice to obtain your OTP bounty. You can use the substrate wallet address starting with 1,5 or g. **Do not use a Ledger Polkadot wallet** as it is not yet compatible with OT Parachain. You can easily create a substrate hot wallet by using [**Polkadot js extension**](https://polkadot.js.org/extension/) **** or [**Talisman**](https://talisman.xyz/)**.** The bounty will be sent out shortly.

{% hint style="warning" %}
**RECOMMENDED**

If you wish to create the most secure substrate wallet to receive your OTP bounty and to map your EVM wallet. Please consult the [**Safe Mapping Guide**](trac-teleportation-faq.md#undefined) **** below.
{% endhint %}

#### 3. Map your wallets&#x20;

You need to visit [**this**](https://parachain.origintrail.io/parachain-account-mapping) interface to map your EVM (Ethereum) wallet to your substrate (Polkadot) wallet in order to receive OTP-native TRAC.

If you want to know why mapping is mandatory, read [**this**](https://docs.origintrail.io/blockchain-layer-1/origintrail-parachain/origintrail-parachain-evm) description by OriginTrail team.&#x20;

{% hint style="warning" %}
The mapping process is **permanent** so make sure you are using the right addresses.
{% endhint %}

On MetaMask, connect to the **OriginTrail Parachain network** and use the correct RPC URL as noted [**here**](https://docs.origintrail.io/blockchain-layer-1/origintrail-parachain/origintrail-parachain-network-rpc#origintrail-parachain-mainnet).&#x20;

{% hint style="info" %}
**Make sure you have at least 2 OTP on your substrate wallet before mapping**. You are required to always hold at least 1 OTP to keep your OT Parachain wallet active and some more OTP for transactions.&#x20;
{% endhint %}

On the mapping interface, select **Mainnet** from the drop down menu, click on **Connect wallet**, and paste your substrate wallet address starting with 1,5 or g, confirm both transactions and you are done!

Here is a short video by the OriginTrail team to help you with mapping your wallets:

{% embed url="https://youtu.be/yltbdB1bpEA" %}

#### 4. Retrieve our teleported TRAC

As of November 18, 2022, users who teleported their TRAC can now follow this [**link** ](https://teleport.origintrail.io/trac-distribution)to see their teleport status. Users who mapped their wallets successfully should see their teleported TRAC on their EVM wallet. Users who did not map their EVM wallet as shown on step 3 will have their teleported TRAC withheld until the mapping is completed.&#x20;

{% hint style="success" %}
If you have completed all previous steps, please import this token to your Metamask address:

0xFfFFFFff00000000000000000000000000000001
{% endhint %}

{% hint style="success" %}
Alternate method: \
Since teleported TRAC is a native Parachain asset, you are able to see your TRAC balance through the polkadot.js portal in the Assets section. After importing your account into the interface, navigate to Network -> Assets -> Balances.
{% endhint %}

## Safe Mapping Guide

{% hint style="warning" %}
### **IMPORTANT**

#### As of October 31, 2022, Branimir has confirmed that Ledger support is [planned and in the works](https://twitter.com/BranaRakic/status/1587094823403753474). I suggest waiting for an official announcement for Ledger support before proceeding any further.&#x20;
{% endhint %}

Most TRAC holders use a hardware (Ledger, Trezor) wallet to store their TRAC for increased security. It is also recommended to use your hardware wallet to teleport your TRAC to keep your funds secure. As long as you hold the keys to your hardware wallet that held your TRAC, you can safely assume that it will be returned back to you once the teleportation is complete.&#x20;

However, once you map a substrate hot wallet (Polkadot JS, Talisman) to your hardware wallet, you completely lose the security net provided by your hardware device.&#x20;

{% hint style="warning" %}
The substrate wallet is a **hot wallet**, just like MetaMask, and any hacker who gets a hold of your substrate wallet will be able to steal all your TRAC or OTP on OT Parachain (other assets held on other chains will not be affected).
{% endhint %}

&#x20;It might very well be an unlikely scenario, but one to consider if you value the utmost safety of your funds.&#x20;

To mitigate mapping risks, I have written a small guide below that uses a **bootable live USB solution**. A bootable live USB is a clean OS environment that you can safely work on, knowing that all files and logs saved are temporary and discarded the moment you reboot your computer. Since mapping allows both EVM and substrate wallets to perform any transactions for both TRAC and OTP on the OT Parachain, you will only need to have one of the two wallets available handily to do any tasks. We will choose our hardware wallet for that as the safer option.

#### Prerequisites:

* 16GB USB drive to create the live OS environment
* Download an **ISO image** to be installed on that USB Stick. Good examples include [**EndeavourOS**](https://endeavouros.com/latest-release/) **** or [**Lubuntu**](https://lubuntu.me/downloads/)
* A tool to create a bootable USB drive such as [**Rufus**](https://rufus.ie/en/) or [**Etcher**](https://www.balena.io/etcher/)
* A good Internet connection to your PC
* A way to send at least 2 OTP to your live OS environment. You will need another PC or a mobile wallet such as Fearless app to make this transaction. Click [**here** ](trac-teleportation-faq.md#undefined)if you are unable to meet this requirement.

#### Instructions:

1. Create a bootable USB drive with one of the tools mentioned above
2. Restart your PC and boot from your USB drive. Depending on your PC, you need to either press F8 or F12 while restarting to load the boot menu.
3. Select Boot EndeavourOS Default or Start Lubuntu. You are now accessing your Live OS environment from within your USB drive.&#x20;
4. To mitigate all risks, visit the least amount of websites possible. Open up FireFox, then Settings, Extensions.
5. Download **Metamask** and **polkadot{.js} extension**
6. Create a new account with MetaMask, you do not need to write down the backup seeds. Then, connect your hardware wallet to Metamask.
7. On the polkadot js extension, create a new wallet, and **write down the 12-word seed phrase and your public wallet**. This is a very important step as you will no longer have easy access to this wallet once you restart your PC.&#x20;
8. Send at least 2 OTP to your newly generated substrate (Polkadot) wallet using another PC or your mobile device.
9. Map your EVM to your substrate wallet by using the mapping website: [https://parachain.origintrail.io/parachain-account-mapping](https://parachain.origintrail.io/parachain-account-mapping)
10. Once both transactions are complete, double check that you have written the 12-word seed phrase for your substrate wallet correctly and restart your PC.&#x20;

Done! This is the most secure way to safeguard your substrate hot wallet, while using your hardware wallet for day-to-day transactions on OT Parachain.

## FAQ

**What does Teleporting TRAC mean exactly ?**

Teleporting TRAC involves locking your ERC-20 TRAC on Ethereum blockchain in a Smart Contract in order to mint the equivalent amount of TRAC on OriginTrail Parachain to be used on the DKG v6 for many different applications - check illustration [here](https://teleport.origintrail.io/) and [OT-RFC-14](https://medium.com/origintrail/ot-rfc-14-dkg-v6-trac-tokenomics-886ff2b6b8cb?source=rss-fecf7416927e------2) for all use cases.

There was an elaborate RFC that was discussed in details [here](https://github.com/OriginTrail/OT-RFC-repository/issues/16). The revised version of the RFC was approved and shown [here](https://medium.com/origintrail/ot-rfc-12-v2-teleporting-trac-to-the-origintrail-parachain-on-polkadot-de535a9d2693)

In summary, it was deemed risky to use a third-party bridge to bridge a large amount of our ERC-20 TRAC over to OT Parachain. In case of a bridge hack, such as the recent [Nomad bridge hack](https://mobile.twitter.com/i/events/1554556780239355905), we would risk losing all bridged TRAC assets forever.

That is why the team, alongside the community, decided to use **Teleportation** in order to safely move ERC-20 TRAC over to OT Parachain, using a smart contract that was thoroughly audited last year during [SFC staking](https://t.co/NYLru2Aqor).

#### **What are the benefits of Teleporting TRAC ?**

There are several benefits to teleporting TRAC over to OT Parachain.

* You receive a small OTP bounty for the amount of TRAC teleported. The bounty amount is shown at the bottom of the page [here](https://teleport.origintrail.io/).
* You can use OTP-native TRAC for staking/delegating, running nodes, publishing assets, keyword staking... Full list on the illustration [here](https://teleport.origintrail.io/)

#### **Teleportation step 4/4 shows “something went wrong, try again”. Did the transaction fail ?**

No, this is most likely a GUI error and not a transaction error. If you were able to confirm the transaction on Metamask and your TRAC is no longer in your wallet, it means the transaction was successful. If the Metamask transaction failed and your TRAC is still in your wallet. Try repeating the steps again after reopening your browser / using incognito mode.

You can verify the transaction by checking your Metamask history or using [this explorer](https://etherscan.io/) and inputting your wallet address to see where your TRAC currently is.

#### **What will happen to my TRAC if I don't teleport ?**

Nothing. TRAC will remain a ERC-20 Token. The Teleportation smart contract is only for those who want to use TRAC on the OT Parachain as soon as DKG v6 hits mainnet.

The team has given hints that in the future DKG v6 capabilities will also move to other blockchains. However, since there is no OTP incentives to use the DKG on other blockchains, we expect most future activities to remain on OT Parachain.

#### **Do I need to keep 1 OTP on my substrate (Polkadot) wallet to receive the OTP bounty for teleporting ?**

No. 1 OTP is only required if you do not fill up the KYC to receive the OTP bounty. If you choose not to KYC, then you will have to find other ways to get 1 OTP in order to use as gas fees to transact with your OTP-native TRAC once you receive it from the Teleportation.

#### **I have teleported my TRAC, where is my OTP-native TRAC now ?**

Please be patient. The team is working on the DKG v6 so it hits mainnet ASAP. As long as v6 isn't live, there is nothing you can do with OTP-native TRAC. Wait for an announcement on how to claim your OTP-native TRAC. The team has recently said the first 2 teleportations were successful so rest assured that they are on the right track.

#### **How long is the Teleportation lock up period and when will I be able to transact my TRAC ?**

Most details should be on the [OT-RFC-12 v2](https://medium.com/origintrail/ot-rfc-12-v2-teleporting-trac-to-the-origintrail-parachain-on-polkadot-de535a9d2693).

Soon after v6 goes live, an OTP-TRAC LP will be available on the OT Parachain to transact between TRAC and OTP.

The lock-up period is approximately 1 year, but I firmly believe LPs such as TRAC/USDT, TRAC/AUSD, OTP/USDT, OTP/AUSD would be available on Acala way before.

Do not quote me on this though as nothing is official :p

#### **Can I use my Ledger/Trezor to Teleport my TRAC ?**

Absolutely. I would go as far to say that is my recommended method of teleporting your TRAC to keep your funds safe.

OT Parachain is EVM compatible and Metamask will be used extensively (as is the case now).

#### How do I check whether my mapping was successful ?&#x20;

In order to verify whether your substrate address is mapped to a given EVM address, go to this [**link** ](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Flofar.origin-trail.network#/chainstate)if you mapped using Devnet, or this [**link** ](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fparachain-rpc.origin-trail.network#/chainstate)if you mapped using Mainnet.&#x20;

1. Go to Developer > Storage tab
2. Choose evmAccounts ->accounts(H160) &#x20;
3. Enter your EVM public key
4. Press + on the right side
5. You should get your substrate public address as a response



**If your question isn't covered here, check out the current official FAQ at the bottom of** [**https://teleport.origintrail.io/**](https://teleport.origintrail.io/) **or feel free to message me @BRX86 on any OriginTrail Telegram channels.**
