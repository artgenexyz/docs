---
description: a.k.a how to mint NFTs on Wix or how to connect Metamask to Wix
---

# 🪄 How to build an NFT minting website on Wix without code

This article helps to set up a no-code widget that allows minting NFTs on your **Wix** website.&#x20;

{% hint style="info" %}
Webflow, WordPress, and Squarespace are also supported. [Click to read Webflow guide](using-webflow-widget.md). For others, instructions are coming soon, meanwhile, [ask in our Discord](https://discord.com/invite/dRg2tGqfhE)
{% endhint %}

### TL;DR

* [ ] Create/open your Wix website
* [ ] Go to Settings -> Advanced -> Custom code, click "**+Add custom code**" (at least "Connect Domain" Wix subscription required)
* [ ] Paste Buildship [code snippet](wix-nft-minting-website.md#how-to-use) to the block, under "Place Code in" **** select **"Body - end"**&#x20;
* [ ] Update code snippet with your contract address [(see below)](wix-nft-minting-website.md#how-to-use)
* [ ] Add a button with URL: `https://your-minting-website.xyz/#mint-button`

### Starting out

* You need an Ethereum NFT smart contract. [Create it using Buildship](https://app.buildship.xyz), or test with an [example contract](https://github.com/buildship-dev/webflow-nft-components#example-for-testing).

{% hint style="success" %}
**ERC721Community** contract by [buildship.xyz](https://buildship.xyz) is used by **280+** collections with **1500ETH+** in total volume. It uses ERC721A, and has **40-100% lower** minting gas fees, costs **\~10-20$ in gas to deploy**, bullet-proof security, and extensions like allowlists, funds/royalty splits, mint passes, etc.
{% endhint %}

* Make sure your contract has `price` and `mint` constants. The possible namings are: `mint`, `buy` or `mintXXX`; `price` or `cost`.
* Your Wix website is at least on a **Connect Domain** site plan (required to add custom code)

### How to use?

1. Open Wix website editor
2. Go to your Wix Dashboard by clicking on Wix logo. Then open Settings -> Advanced -> Custom code, and click on "**+ Add custom code**" button

![Dashboard Settings -> Advanced -> Custom code](<../.gitbook/assets/image (2).png>)

&#x20; 3\. Copy & paste this code in the Wix window, and select the **"Body - end"** option under **"Place Code in".**

**Don't close the code window, we'll still need it in Step 4.**

```html
<script>
   CONTRACT_ADDRESS = "YOUR CONTRACT ADDRESS HERE"
   IS_TESTNET = false
   // if your contract is NOT VERIFIED on Etherscan
   // put here: CONTRACT_ABI = [{...}]
   // don't do anything if unsure
</script>
<script src="https://nftcomponents.vercel.app/static/js/main.js"></script>
<link href="https://nftcomponents.vercel.app/static/css/main.css" rel="stylesheet">
```

&#x20; 4\. If you **have your Ethereum NFT contract**

* [ ] insert your contract address in `CONTRACT_ADDRESS` field
* [ ] set `IS_TESTNET` to `false` or `true` depending on which network is the contract on: `Ethereum Mainnet` or `Goerli Testnet`.

If you **don't have a contract**, [create it using Buildship](https://app.buildship.xyz) without coding skills

> Your contract should be [verified](https://etherscan.io/verifyContract) on [Etherscan](https://etherscan.io). Otherwise you have to add `CONTRACT_ABI = [{...}]` line in the above code, with your full contract ABI inserted. If you have an error saying your ABI is too long, [click here](https://github.com/buildship-dev/webflow-nft-components/issues/22#issuecomment-1042708174).

&#x20; 5\. Create a Wix button and insert your minting page link ending with `/#mint-button`.&#x20;

Example: `https://your-minting-website.xyz/#mint-button`

Then set the **"How does it open?"** option to **"Current window"**.

![Creating a button in Wix editor](<../.gitbook/assets/image (3).png>)

![My minting page URL is https://theshad.wixsite.com/minting-website, so look](<../.gitbook/assets/image (4).png>)

&#x20; 6\. Publish the changes, and you're done 🎉

#### Example for testing

```html
<script>
   CONTRACT_ADDRESS = "0xb1db0dbad7a14370872a7e5327c8ad7c9951a661"
   IS_TESTNET = true
</script>
<script src="https://nftcomponents.vercel.app/static/js/main.js"></script>
<link href="https://nftcomponents.vercel.app/static/css/main.css" rel="stylesheet">
```

### FAQ

#### I'm confused / it's not working, can you help me?

Yes, absolutely! You can [contact us in Discord](http://buildship.xyz), or open a [GitHub issue](https://github.com/buildship-dev/webflow-nft-components/issues/new)

#### How to use this with Polygon, Binance, or other Ethereum-based networks?

It's easy! Set `NETWORK_ID` instead of `IS_TESTNET` in the code snippet

```html
<script>
   CONTRACT_ADDRESS = "YOUR CONTRACT ADDRESS HERE"
   NETWORK_ID = 1
   // remove IS_TESTNET line
   ...
</script>
<script ...>
<link ...>
```

Some of the network IDs you might use:

* Ethereum Mainnet: `NETWORK_ID = 1`
* Ethereum Rinkeby Testnet: `NETWORK_ID = 4`
* Polygon: `NETWORK_ID = 137`
* Binance: `NETWORK_ID = 56`
* For other IDs visit [Chainlist](https://chainlist.org)

#### How to style minting dialog?

[See the example here](https://github.com/buildship-dev/webflow-nft-components/wiki/Mint-button-widget#how-to-style-minting-dialog)

#### How to hide minted counter from the dialog?

You need to set `DEFAULTS.hideCounter` to `true`

```html
<script>
   CONTRACT_ADDRESS = "YOUR CONTRACT ADDRESS HERE"
   NETWORK_ID = 1
   DEFAULTS = {
       hideCounter: true
   }
   ...
</script>
<script ...>
<link ...>
```

