---
description: Step-by-step guide to run a V6 Testnet Node
---

# V6 Testnet Migration Guide

## Instructions

{% hint style="danger" %}
### If you are a V6 **Devnet** Node runner already, please do step 2-3-4-5-7 only in the correct order.
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

Gather the following information:

* **EVM Operational wallet private key** (private key from wallet 1 in step 1)
* **EVM Management wallet private key** (private key from wallet 2 in step 1)
* **Hub Contract Address**
  * This is found in the logs of your node, but should be **0xEF9FeCb85d03d6e624C434dF8298692d13853033** default for now.&#x20;

Navigate to the current ot-node version folder:

```
cd /root/ot-node/current
```

Once **** you have all the information above, run the following command by replacing the values in <> with the correct information:

Set the stake of your node:

```
npm run set-stake -- --rpcEndpoint=https://lofar-testnet.origin-trail.network/ --stake=50000 --operationalWalletPrivateKey=<private_key> --managementWalletPrivateKey=<private_key> --hubContractAddress=0xEF9FeCb85d03d6e624C434dF8298692d13853033
```

Set the service ask of your node:

```
npm run set-ask -- --rpcEndpoint=https://lofar-testnet.origin-trail.network/ --ask=0.0002 --privateKey=<operational_wallet_private_key> --hubContractAddress=0xEF9FeCb85d03d6e624C434dF8298692d13853033
```

Once you are done, restart the node:

```
systemctl restart otnode
```

Check the logs, you should be done:

```
journalctl -u otnode --output cat -fn 100
```

If you have any questions concerning this guide, please contact me on Telegram **@BRX86**.

## 2022-12-08 Update:

For those who are already running a test node, you need to get another 50k TRAC from the Discord bot of from me **@BRX86**, stop the node and then edit the node config file:&#x20;

```
systemctl stop otnode
```

```
nano /root/ot-node/.origintrail_noderc
```

Spam ctrl+k to delete the current config, then paste the following:&#x20;

```
{
    "logLevel": "trace",
    "auth": {
        "ipWhitelist": [
            "::1",
            "127.0.0.1"
        ]
    },
    "modules": {
        "tripleStore": {
            "defaultImplementation": "ot-blazegraph"
        },
        "blockchain": {
            "defaultImplementation": "otp",
            "implementation": {
                "otp": {
                    "config": {
                        "sharesTokenSymbol": "random_token_symbol_here",
                        "sharesTokenName": "random_token_name_here", 
                        "rpcEndpoints": [
                            "https://lofar-testnet.origin-trail.network/", "wss://parachain-testnet-rpc.origin-trail.network"
                        ],
                        "evmOperationalWalletPublicKey": "evm_op_address_here",
                        "evmOperationalWalletPrivateKey": "evm_op_privatekey_here",
                        "evmManagementWalletPublicKey": "evm_management_address_here",
            "evmManagementWalletPrivateKey": "evm_management_privatekey_here"
                    }
                }
            }
        },
        "network": {
            "implementation": {
                "libp2p-service": {
                    "config": {
                        "privateKey": ""
                    }
                }
            }
        }
    }
}
```

{% hint style="info" %}
```
Make sure you replace the following wih the correct values on your node config above:
random_token_symbol_here
random_token_name_here
evm_op_address_here
evm_op_privatekey_here
evm_management_address_here
evm_management_privatekey_here
```
{% endhint %}

Restart the node to create the profile

```
systemctl restart otnode
```

After the profile is created, stop the node again:

```
systemctl stop otnode
```

You need to run step 7 set-stake set-ask scripts again:

{% hint style="danger" %}
The Hub contract address has changed. Make sure you run the 2 scripts in Step 7 again with the new correct Hub contract address.&#x20;
{% endhint %}

Once you are done,

```
systemctl restart otnode
```

## DEBUG

* Step2-5: if you were only able to get test OTP and not test TRAC, contact me on Discord on Telegram and I will send you some test TRAC.&#x20;
* Step 4: If mapping doesn't prompt you with 2 transactions, try disabling all other extensions and restart your browser. You can also use a different browser. Choose between Chrome, Brave, Firefox.
* Step 7: if you were unable to run the npm set stake script and this error shows up:\
  submit transaction to pool failed: Pool(InvalidTransaction(InvalidTransaction::Payment)\
  Then, go to folder /root/ot-node/6.0.0-beta.3.1.2 rather than /root/ot-node/current
