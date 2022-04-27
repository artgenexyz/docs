---
description: a.k.a how to connect Metamask to Webflow
---

# 🐧 How to mint NFTs on Webflow without code

This article helps to set up a no-code widget that allows minting NFTs on your **Webflow** website.&#x20;

{% hint style="info" %}
Wix, WordPress, and Squarespace are also supported. Instructions coming soon, meanwhile, [ask in our Discord](https://discord.com/invite/dRg2tGqfhE)
{% endhint %}

### TL;DR

* [ ] Open Webflow website and subscribe to the **Basic** site plan
* [ ] Add a button with id = `mint-button`
* [ ] Create an "Embedded HTML code" block in Webflow
* [ ] Paste [code snippet](using-webflow-widget.md#how-to-use) to the block
* [ ] Update code snippet with your contract address (see below)

You can also [clone our free Webflow minting template](https://webflow.com/website/Free-NFT-minting-website-template-from-buildshipxyz) to use it as an example

### Starting out

* You need an Ethereum NFT smart contract. [Contact us to deploy it using Buildship](https://buildship.xyz), or test with an [example contract](https://github.com/buildship-dev/webflow-nft-components#example-for-testing).

{% hint style="success" %}
**MetaverseNFT** contract by [buildship.xyz](https://buildship.xyz) is used by **40+** collections with **1500ETH+** in total volume. It features **40% lower** mint gas fees, costs **\~100$ in gas to deploy**, bullet-proof security, and extensions like presale lists, mint passes, etc.

Create your contract
{% endhint %}

* Make sure your contract has `price` and `mint` functions. The possible namings are: `mint`, `buy` or `mintXXX`; `price` or `cost`.
* Your Webflow website is at least on a **Basic** site plan (required to add custom code blocks)

### How to use?

1. Open Webflow website editor
2. Create a new [Embedded HTML code](https://university.webflow.com/lesson/custom-code-embed) block (at least **Basic** site plan required)
3. Copy & paste this code in Webflow Embed block

```html
<script>
   CONTRACT_ADDRESS = "<your contract address here>"
   IS_TESTNET = false
   MAX_PER_MINT = 20
   // place to put CONTRACT_ABI = [{...}]
</script>
<script src="https://nftcomponents.vercel.app/static/js/main.js"></script>
<link href="https://nftcomponents.vercel.app/static/css/main.css" rel="stylesheet">
```

1. If you **have your Ethereum NFT contract**
   * [ ] insert your contract address in `CONTRACT_ADDRESS` field
   * [ ] set `IS_TESTNET` to `false` or `true` depending on which network is the contract on: `Ethereum Mainnet` or `Rinkeby Testnet`.

If you **don't have a contract**, [contact us to deploy using Buildship](https://buildship.xyz)

> Your contract should be [verified](https://etherscan.io/verifyContract) on [Etherscan](https://etherscan.io). Otherwise you have to add `CONTRACT_ABI = [{...}]` line in the above code, with your full contract ABI inserted. If you have an error saying your ABI is too long, [click here](https://github.com/buildship-dev/webflow-nft-components/issues/22#issuecomment-1042708174).

1. Create a button with ID `mint-button` on your Webflow site

If you can't set an ID, you can set a button URL as `#mint-button` or `https://<your-website-url>/#mint-button`

1. You're done 🎉

#### Example for testing

```html
<script>
   CONTRACT_ADDRESS = "0x8Fac2e25DFF0B248A19A66Ae8D530613c8Ff670B"
   IS_TESTNET = true
   MAX_PER_MINT = 20
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
   CONTRACT_ADDRESS = "<your contract address here>"
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
   CONTRACT_ADDRESS = "<your contract address here>"
   NETWORK_ID = 1
   DEFAULTS = {
       hideCounter: true
   }
   ...
</script>
<script ...>
<link ...>
```

