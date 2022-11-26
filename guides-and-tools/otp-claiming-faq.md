---
description: Everything about claiming OTP rewards
---

# OTP Claiming FAQ

### This guide is expired as of September 2022 since the OTP claiming process is completed. I hope it was helpful while it lasted!

### TABLE OF CONTENT

[**INTRODUCTION**](otp-claiming-faq.md#0-introduction)****

****[**IMPORTANT GENERAL NOTES**](otp-claiming-faq.md#1-important-general-notes)

****[**AM I ELIGIBLE FOR TRAC HOLDER OTP REWARD ?**](otp-claiming-faq.md#2-am-i-eligible-for-trac-holder-otp-reward)

****[**HOW DO I CLAIM MY V5 NODE RUNNER OTP REWARD ? (ALREADY DISTRIBUTED 2022-08-08)**](otp-claiming-faq.md#3-how-do-i-claim-my-v5-node-runner-otp-reward)

****[**THE CLAIMING INTERFACE USES METAMASK AND MY FUNDS ARE ELSEWHERE, WHAT DO I DO ?**](otp-claiming-faq.md#4-the-claiming-interface-uses-metamask-and-my-funds-are-held-elsewhere-what-do-i-do)

****[**HOW TO CLAIM YOUR VESTED AMOUNT OF OTP**](otp-claiming-faq.md#5-how-to-claim-your-vested-amount-of-otp)

****[**RECOMMENDED POLKADOT WALLETS**](otp-claiming-faq.md#recommended-polkadot-wallets)

****[**HOW TO CHECK YOUR OTP BALANCE**](otp-claiming-faq.md#how-to-check-your-otp-balance)

### INTRODUCTION

Hello, this is BRX from the OT community. I will keep updating this page so keep it handy for the future. Claiming OTP is an elaborate process for the average user. Therefore, I made this page to simplify every process. If you have any questions, feel free to @BRX86 on TG and I should be quick to answer your question.

#### Before proceeding, you shoud first read the [**official claiming instructions**](https://medium.com/origintrail/otp-distribution-process-explained-2878a440d9d7)

### IMPORTANT GENERAL NOTES

1. **DO NOT USE YOUR LEDGER POLKADOT ADDRESS**, it is not compatible with parachains and you will not be able to move your OTP around. If you already used your Ledger Polkadot Address to claim OTP, you can export the 12-word seed from your ledger to a compatible DOT wallet (see section \[6])
2. You can use any type of Polkadot wallet address on the application forms (address can start with 1, 5, or a letter) This is valid for both TRAC holder OTP reward and v5 node runner OTP reward forms.
3. You must keep at least 1 OTP AT ALL TIMES on your OTP wallet address after receiving the initial OTP reward. This allows for your OTP wallet address to remain active and to be able to claim vested amounts later on.
4. You do NOT need to have 1 DOT on your Polkadot wallet, you only need to keep at least 1 OTP.

### AM I ELIGIBLE FOR TRAC HOLDER OTP REWARD ?

1. You must have held TRAC at the time of the snapshot that was done on May 18th 2022 08:45:22 (Ethereum block 14800965)
2. You must have held your TRAC on any chain (ETH, Polygon, DAI) but in a SELF CUSTODY WALLET (ledger, trezor, metamask, MEW, other erc20 wallets) meaning you held the private keys.
3. You are NOT eligible to receive OTP rewards if you held your TRAC on an exchange, in OT nodes, or on Bancor.
4. You have from now until September 29th 2022 to claim your TRAC holder OTP reward.
5. If you held TRAC in more than one chain (eth TRAC, xTRAC, mTRAC), you need to check if the TRAC on each chain was held using the same Metamask wallet address. If so, you only need to enter it once to be eligible for the OTP reward. If not, you need to enter each address to be eligible for each of them.

Once you are ready, head to [https://parachain.origintrail.io/claim-otp?type=trac-holders](https://parachain.origintrail.io/claim-otp?type=trac-holders), connect to Metamask and select your wallet (check out point \[4] if your wallet isn't compatible with Metamask). Paste your Polkadot wallet address and click apply. You can generate a DOT address using the Talisman extension (see point \[6]).

Currently, distributions are done on a weekly basis so check back a week later once you submitted your form !

### HOW DO I CLAIM MY V5 NODE RUNNER OTP REWARD ?

**ATTENTION: THIS REWARD HAS ALREADY BEEN DISTRIBUTED ON AUGUST 8, 2022**

1. You must have had an active v5 OT node running between March 23rd 2021 and March 23rd 2022
2. You can look for your Node ID (not erc725 ID) on othub [https://othub.origin-trail.network/dashboard](https://othub.origin-trail.network/dashboard)
3. Another way to look for your Node ID is through your current node, do the following commands to show the identity on your logs : docker logs --since 72h otnode | grep "My network identity" (Note : the identity starting with 0x is your erc725 identity, not your node ID)
4. You can use your operational wallet to claim your OTP, you can find that on your config file using this command on your node : nano /root/.origintrail\_noderc \*\*\* If you lost your operational wallet, you can also use your management wallet \*\*\*
5. The claiming interface will be open from July 4th 2022 until July 31st 2022. It will not be possible to apply for DKG v5 node runner rewards after that date.

Once you are ready, head to [https://parachain.origintrail.io/claim-otp?type=node-runners](https://parachain.origintrail.io/claim-otp?type=node-runners) and fill up the form.

### THE CLAIMING INTERFACE USES METAMASK AND MY FUNDS ARE HELD ELSEWHERE, WHAT DO I DO ?

First of all, you are still eligble for the OTP reward. Unfortunately, when we were told we could hold TRAC in any self-custody wallet, we weren't told that it would be much easier if that wallet would be compatible with Metamask. There are NO other ways to claim OTP outside of using Metamask. So anything that can connect to it easily, such as a Ledger of Trezor, would not have to go through the trouble below.

**IMPORTANT: DO NOT send your TRAC over to Metamask, the snapshot was made when your funds were on your initial wallet so you must import the seed phrase of that wallet over to Metamask for the OTP claiming process to work**

Note that the steps below contains risks of exposing your seed phrase to the Internet. Make sure your computer is safe and double check every step.

STEPS TO EXPORT YOUR ACCOUNT OVER TO METAMASK:

_Note that if you already have Metamask extension installed, the steps below will not work. I suggest you use another browser (Firefox if you are currently using Chrome) and install a brand new Metamask extension there first, and then follow the instructions below. Once you are done, you can safely uninstaill Metamask and the whole browser._

1. On your wallet that contained TRAC when the snapshot happened, generate and copy your 12-word seed phrase
2. Install Metamask on your browser: [https://metamask.io/](https://metamask.io/)
3. Paste your 12-word seed from step 1 when creating your Metamask account \*\*\* If you want to be 100% safe, you can move your funds away to another safe wallet address before exporting the seed phrase to Metamask. Since the snapshot was already done, you do not need to hold anything on the wallet you are exporting over to Metamask - it can be completely empty and you will still be able to claim your OTP.
4. Connect your Metamask with the imported wallet to the interface and paste your Polkadot wallet address.

### HOW TO CLAIM YOUR VESTED AMOUNT OF OTP

You will receive 25% of your OTP first, then you can claim the remaining 75% gradually over the course of the parachain lease period of 2 years.

To claim that 75%:

1. you need to have either polkadot js extension installed on your browser or talisman extension
2. Go to [https://polkadot.js.org](https://polkadot.js.org/)
3. Select the OT Parachain network by clicking on the top left corner, then click Switch
4. On the Accounts tab, you should see your OTP balance. Click the 3 vertical dots and select unlock vested amount.
5. Proceed by paying a small OTP gas fee to unlock your current unlockable balance

### RECOMMENDED POLKADOT WALLETS

Only a few wallets are directly compatible with [https://polkadot.js.org](https://polkadot.js.org/)

I strongly suggest using Talisman as it's much more user-friendly than polkadot js extension.

#### Desktop:

Talisman extension: [https://talisman.xyz/](https://talisman.xyz/)

polkadot js extension: [https://polkadot.js.org/extension/](https://polkadot.js.org/extension/)

#### Mobile:

Fearless wallet: [https://fearlesswallet.io/](https://fearlesswallet.io/)

### HOW TO CHECK YOUR OTP BALANCE

In order to check your OTP balance on browser, go to:

1. [https://origintrail.polkaholic.io/chains#chains](https://origintrail.polkaholic.io/chains#chains)
2. Input your Polkadot wallet address (can start with 1, 5 or g)
3. Click on Origin Trail (the pink bar) and you should see your balance

Alternative way: In \[5], do from step 1 to step 3.

