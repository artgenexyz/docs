---
description: a.k.a how to mint NFTs on Webflow or how to connect Metamask to Webflow
---

# 🐧 How to build an NFT minting website on Webflow without code

This article helps to set up a no-code widget that allows minting NFTs on your **Webflow** website.&#x20;

{% hint style="info" %}
Wix, WordPress, and Squarespace are also supported. [Click to read Wix guide.](wix-nft-minting-website.md) Instructions for others coming soon, meanwhile, [ask in our Discord](https://discord.com/invite/dRg2tGqfhE)
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=4MMylTzzwAg" %}
Video guide on using Buildship mint button
{% endembed %}

### TL;DR

* [ ] Open your Webflow website and subscribe to the **Basic** site plan
* [ ] Add a button with id = `mint-button`
* [ ] Create an "Embedded HTML code" block in Webflow
* [ ] Paste [code snippet](using-webflow-widget.md#how-to-use) to the block
* [ ] Update code snippet with your contract address (see below)

You can also [clone one of our free Webflow minting templates](https://webflow.com/theshadeth) and use as an example

### Starting out

* You need an Ethereum NFT smart contract. [Create it using Buildship](https://app.buildship.xyz), or test with an [example contract](https://github.com/buildship-dev/webflow-nft-components#example-for-testing).

{% hint style="success" %}
**ERC721Community** contract by [buildship.xyz](https://buildship.xyz) is used by **280+** collections with **1500ETH+** in total volume. It uses ERC721A, and has **40-100% lower** minting gas fees, costs **\~10-20$ in gas to deploy**, bullet-proof security, and extensions like allowlists, funds/royalty splits, mint passes, etc.
{% endhint %}

* Make sure your contract has `price` and `mint` constants. The possible namings are: `mint`, `buy` or `mintXXX`; `price` or `cost`.
* Your Webflow website is at least on a **Basic** site plan (required to add custom code blocks)

### How to use?

1. Open Webflow website editor
2. Create a new [Embedded HTML code](https://university.webflow.com/lesson/custom-code-embed) block (at least **Basic** site plan required)
3. Copy & paste this code in Webflow Embed block

```html
<script>
   CONTRACT_ADDRESS = "YOUR CONTRACT ADDRESS HERE"
   IS_TESTNET = false
   // place to put CONTRACT_ABI = [{...}]
</script>
<script src="https://nftcomponents.vercel.app/static/js/main.js"></script>
<link href="https://nftcomponents.vercel.app/static/css/main.css" rel="stylesheet">
```

&#x20; 4\. If you **have your Ethereum NFT contract**

* [ ] insert your contract address in `CONTRACT_ADDRESS` field
* [ ] set `IS_TESTNET` to `false` or `true` depending on which network is the contract on: `Ethereum Mainnet` or `Goerli Testnet`.

If you **don't have a contract**, [create it using Buildship](https://app.buildship.xyz) without coding skills

> Your contract should be [verified](https://etherscan.io/verifyContract) on [Etherscan](https://etherscan.io). Otherwise you have to add `CONTRACT_ABI = [{...}]` line in the above code, with your full contract ABI inserted. If you have an error saying your ABI is too long, [click here](https://github.com/buildship-dev/webflow-nft-components/issues/22#issuecomment-1042708174).

&#x20; 5\. Create a button with ID `mint-button` on your Webflow site

If you can't set an ID, you can set a button URL as `#mint-button` or `https://<your-website-url>/#mint-button`

&#x20; 6\. You're done 🎉

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

#### How to add "Connect wallet" button?

Mint button will ask to connect wallet, so it's not necessary to add a "Connect wallet" button.

If you still want to do it, create a Webflow button with ID `connect`.

#### How to add a custom minted counter?

Just create two text elements and assign them:

* `minted-counter` ID to display minted number
* `total-counter` ID to display collection size

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

