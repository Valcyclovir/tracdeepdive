---
description: Step-by-step guide to run a V6 Mainnet Node
---

# V6 Mainnet Node Instructions

## Step 1 - Create a total of 4 wallets

You must create a total of 4 wallets for the following step.&#x20;

<table><thead><tr><th data-type="number">#</th><th>Wallet</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>EVM Operational wallet</td><td>Hot wallet for non admin node operations<br>Example: Metamask wallet</td></tr><tr><td>2</td><td>EVM Management wallet</td><td>Cold wallet for admin node operations<br>Example: Ledger</td></tr><tr><td>3</td><td>Substrate Operational wallet</td><td>Hot wallet to map with wallet #1<br>Example: polkadot.js, Talisman wallet</td></tr><tr><td>4</td><td>Substrate Management wallet</td><td>Cold wallet to map with wallet #2<br>Example: Ledger</td></tr></tbody></table>

{% hint style="warning" %}
Mapping a hardware EVM wallet (such as Ledger) to a hot substrate wallet (such as polkadot.js or Talisman wallet) could expose your funds to the Internet since both EVM and substrate wallets can have full access to your funds on the Polkadot Ecosystem. Waiting for OTP Ledger support before mapping is strongly advised to protect your funds. \
\
For the time being, the safest method to run a mainnet node is highlighted in the [**temporary safe method to run a mainnet node**](v6-testnet-migration-guide.md#temporary-safe-mainnet-node-instructions) section.&#x20;
{% endhint %}

## Step 2 - Add the OriginTrail Mainnet Network onto MetaMask

By using the information found [**here**](https://docs.origintrail.io/blockchain-layer-1/origintrail-parachain/origintrail-parachain-networks#origintrail-parachain-mainnet), add the OriginTrail Mainnet Network on your MetaMask client and switch to it.&#x20;

## Step 3 - Fund your wallets with OTP

Fund your wallets in step 1 with OTP tokens. For example, you can use TRAC holder OTP reward or teleport OTP bounty to fund your wallets.&#x20;

You can also ask for some dust on [**OriginTrail Node Community**](https://t.me/otnodegroup)**.** You need at least 2 OTP (1 OTP for ED amount and the other for transations) on your substrate wallets (wallet **3 and 4** from step 1)

## Step 4 - Map your wallets

Once the funding of both substrate wallets are completed, head to the [**mapping interface**](https://parachain.origintrail.io/parachain-account-mapping) **** and select **Parachain Mainnet**.&#x20;

Your goal here is to map wallet **1 and** **3** together, and wallet **2 and 4** together from step 1.&#x20;

To do so, connect to the mapping interface with the appropriate MetaMask wallet and paste the corresponding substrate wallet. 2 pop-ups will follow and sign both transactions.

{% hint style="warning" %}
If mapping doesn't prompt you with 2 transactions, try disabling all other extensions and restart your browser. You can also use a different browser. Choose between Chrome, Brave, Firefox.
{% endhint %}

Repeat for wallet **2 and 4** from step 1 and you would have completed the mapping process for your node.&#x20;

## Step 5 - Fund your wallets with teleported TRAC

You require a minimum of 50k TRAC to run a mainnet node. You can purchase TRAC on **** [**Coinbase**](https://www.coinbase.com/price/origintrail)**,** [**Kucoin**](https://www.kucoin.com/trade/TRAC-BTC)**,** [**Huobi**](https://www.huobi.com/en-us/exchange/trac\_usdt/)**,** [**Uniswap**](https://app.uniswap.org/#/swap?outputCurrency=0xaa7a9ca87d3694b5755f213b5d04094b8d0f0a6f) **** and **** [**others**](https://www.coingecko.com/en/coins/origintrail#markets)**.**&#x20;

Once the TRAC token is acquired, you must [**teleport**](http://teleport.origintrail.io) your tokens to the OriginTrail Parachain in order to use them on the parachain. Follow the [**Teleportation Guide**](trac-teleportation-faq.md) for a complete set of instructions.&#x20;

{% hint style="info" %}
**Reminder**:&#x20;

OTP is used as gas to send teleported TRAC so always have at least 2 OTP on each wallet containing teleported TRAC.&#x20;
{% endhint %}

To view your TRAC balance on Metamask, first switch your network to OriginTrail Parachain Network, then add the TRAC token address using the import function

```
0xFfFFFFff00000000000000000000000000000001
```

You can also view your test TRAC on polkadot.js [**here**](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fparachain-rpc.origin-trail.network#/assets/balances).&#x20;

## Step 6 - Install your node

In order to deploy your OriginTrail V6 node, you will need a Linux server with the following minimum recommended hardware:

* **4GB RAM**
* **2CPUs**
* **50GB HDD space**

{% hint style="warning" %}
Log in to the server as root. You **cannot** use sudo and run this script. The command "**npm ci**" might fail.
{% endhint %}

Gather the following information:

| Value                          | Description                           |
| ------------------------------ | ------------------------------------- |
| EVM\_OPERATIONAL\_WALLET       | Public address of wallet #1 in step 1 |
| EVM\_OPERATIONAL\_PRIVATE\_KEY | Private key of wallet #1 in step 1    |
| EVM\_MANAGEMENT\_WALLET        | Public address of wallet #2 in step 1 |
| SHARES\_TOKEN\_NAME            | Your choice of token name             |
| SHARES\_TOKEN\_SYMBOL          | The token symbol of your token name   |

**Run the one-liner installer script:**

```
cd /root/ && curl https://raw.githubusercontent.com/OriginTrail/ot-node/v6/release/mainnet/installer/installer.sh --output installer.sh && chmod +x installer.sh && ./installer.sh
```

{% hint style="danger" %}
You must choose a SQL password for the installer to work. Do not leave that field empty.
{% endhint %}

{% hint style="info" %}
**Reminder**:&#x20;

In order to use aliases to quickly check node logs, start/stop/restart node, change node config, you must execute the following script after the installation:

\
source \~/.bashrc



Once the sourcing is done, try the following:\
otnode-logs

otnode-start

otnode-stop

otnode-restart

otnode-config
{% endhint %}

## Step 7 - Set-stake and set-ask

The installer above will only set up all the prerequisites and node files. You must run 2 scripts to create the node profile and set your service ask price.&#x20;

First, stop the node:

```
systemctl stop otnode
```

Gather the following information:

| Value                                  | Description                                                                                                                                                                                                                                                                      |
| -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **EVM Operational wallet private key** | private key from wallet 1 in step 1                                                                                                                                                                                                                                              |
| **EVM Management wallet private key**  | private key from wallet 2 in step 1                                                                                                                                                                                                                                              |
| **Hub Contract Address**               | <p><strong>0x5fA7916c48Fe6D5F1738d12Ad234b78c90B4cAdA</strong><br><strong></strong>Check the official <a href="https://docs.origintrail.io/blockchain-layer-1/origintrail-parachain/deployed-smart-contracts"><strong>link</strong></a> to make sure it is the correct one. </p> |
| **Ask price**                          | <p>Your price as a node runner to host assets. <br>Team default: 0.00375/(epoch * KB)</p>                                                                                                                                                                                        |
| **rpcEndpoint**                        | [https://astrosat-parachain-rpc.origin-trail.network/](https://astrosat-parachain-rpc.origin-trail.network/)                                                                                                                                                                     |
| **Stake**                              | <p>Your initial stake for your node <br>(minimum: 50000)</p>                                                                                                                                                                                                                     |

Navigate to the current ot-node version folder:

```
cd /root/ot-node/current
```

Once **** you have all the information above, run the following command by replacing the values in <> with the correct information (you can also change the other options if needed):

Set the **stake** of your node:

```
npm run set-stake -- --rpcEndpoint=https://astrosat-parachain-rpc.origin-trail.network/ --stake=50000 --operationalWalletPrivateKey=<private_key> --managementWalletPrivateKey=<private_key> --hubContractAddress=0x5fA7916c48Fe6D5F1738d12Ad234b78c90B4cAdA
```

Set the **service ask** of your node:

```
npm run set-ask -- --rpcEndpoint=https://astrosat-parachain-rpc.origin-trail.network/ --ask=0.00375 --privateKey=<operational_wallet_private_key> --hubContractAddress=0x5fA7916c48Fe6D5F1738d12Ad234b78c90B4cAdA
```

Once you are done, restart the node:

```
systemctl restart otnode
```

{% hint style="success" %}
This is when your initial stake of 50k TRAC or above is sent from your initial wallet to your node profile contract.&#x20;
{% endhint %}

Check the logs, everything should be completed!

```
journalctl -u otnode --output cat -fn 100
```

{% hint style="info" %}
**Reminder:**

You can now use aliases such as otnode-logs to quickly view logs without having to type the entire string above!
{% endhint %}

## Temporary Safe Mainnet Node Instructions

1.  Use the instructions [**here**](https://deepdive.origintrail.club/guides-and-tools/trac-teleportation-faq#safe-mapping-guide) **** to pair 3 wallets.

    1. 1 main wallet pair to receive your teleported TRAC and OTP bounty
    2. 1 operational wallet pair for your node
    3. 1 management wallet pair for your node


2. Receive your teleported TRAC and OTP bounty on main mapped wallet (wallet #1 above)
3. Send some teleported TRAC to management evm wallet (wallet #3 above), and some OTP to op / management wallets
4. Set up your node following the instructions above
5. When OTP is supported by ledger, change your management and operational wallet addresses to a brand new ledger evm + ledger otp mapped wallet
