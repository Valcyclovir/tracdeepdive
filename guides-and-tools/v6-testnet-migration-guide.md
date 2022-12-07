---
description: Step-by-step guide to run a V6 Testnet Node
---

# V6 Testnet Migration Guide

## Instructions

{% hint style="warning" %}
If you are coming from a V6 **Devnet** Node, please skip all the way to step
{% endhint %}

### Step 1 - Create a total of 4 wallets

You must create hot wallets on [**MetaMask**](https://metamask.io/) **** and [**Dot js extension**](https://polkadot.js.org/extension/) **** / [**Talisman**](https://talisman.xyz/) for the following step.&#x20;

1. EVM Operational (MetaMask) wallet
2. EVM Management (MetaMask) wallet
3. Substrate Operational (Polkadot) wallet
4. Substrate Management (Polkadot) wallet

This step is crucial for the mapping process in step 4.&#x20;

### Step 2 - Add the OriginTrail Testnet Network onto MetaMask

By using the information found [**here**](https://docs.origintrail.io/blockchain-layer-1/origintrail-parachain/origintrail-parachain-networks#origintrail-parachain-testnet), add the OriginTrail Testnet Network on your MetaMask client and switch to it.&#x20;

### Step 3 - Fund your wallets with test OTP

Fund your wallets in step 1 with test OTP tokens.&#x20;

Go on [**Discord**](https://discord.com/channels/460837319025623050/938284634477834270) **** and use the bot to ask for test OTP tokens as follows:

`!fundme_otp`` `_`<substrate_wallet_address`_`>`

You can also ask for test OTP tokens on [**OriginTrail Node Community**](https://t.me/otnodegroup)****

{% hint style="success" %}
Make sure you have test OTP on both substrate wallets (wallets 3 and 4 on step 1). You can send some test OTP you received from the Discord bot earlier by going on [**polkadot.js**](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fparachain-testnet-rpc.origin-trail.network%2F#/accounts) **** and clicking on the **Send** button.&#x20;
{% endhint %}

### Step 4 - Map your wallets

Once the funding of both substrate wallets are completed, head to the [**mapping interface**](https://parachain.origintrail.io/parachain-account-mapping) **** and select **Parachain Testnet**.&#x20;

Your goal here is to map wallet **1 and** **3** together, and wallet **2 and 4** together from step 1.&#x20;

To do so, connect to the interface with the appropriate MetaMask wallet and paste the corresponding substrate wallet. 2 pop-ups will follow and sign both transactions.

Repeat for wallet 2 and 4 from step 1 and you have completed the mapping process for the Testnet.&#x20;

### Step 5 - Fund your wallets with test TRAC

Now that your wallets are mapped, you can now ask the **** [**Discord**](https://discord.com/channels/460837319025623050/938284634477834270) bot for test TRAC.&#x20;

`!fundme_otp_trac`` `_`<evm_management_wallet_address`_`>`

{% hint style="success" %}
Make sure you ask for test TRAC on your **EVM management** wallet address (wallet 2 in step 1). You do not need test TRAC on your EVM operational wallet.&#x20;
{% endhint %}

To view your test TRAC balance on Metamask, first switch your network to OriginTrail Parachain Network, then add the test TRAC token address using the import function

```
0xFfFFFFff00000000000000000000000000000001
```

{% hint style="success" %}
You can also view your test TRAC on polkadot.js [**here**](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fparachain-testnet-rpc.origin-trail.network%2F#/assets/balances).&#x20;
{% endhint %}

### Step 6 - Install your node

{% hint style="warning" %}
Login to the server as root. You **cannot** use sudo and run this script. The command "**npm ci**" might fail.
{% endhint %}

**Run the installer script:**

```
cd /root && wget https://raw.githubusercontent.com/Valcyclovir/testnet/main/installerv2.sh && chmod +x installerv2.sh && ./installerv2.sh
```

### Step 7 - Migrate the Node to Testnet

{% hint style="success" %}
For V6 **Devnet** node runners migrating to **Testnet**, make sure you restart the node to get the latest updates. Once the updates are completed, stop the node.
{% endhint %}

Once the node is installed, stop the node:

```
systemctl stop otnode
```

Navigate to the current ot-node version folder:

```
cd /root/ot-node/current
```

Gather the following information:

* **EVM Operational wallet private key** (private key from wallet 1 in step 1)
* **EVM Management wallet private key** (private key from wallet 2 in step 1)
*

****

****



```
```
