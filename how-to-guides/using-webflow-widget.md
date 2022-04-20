---
description: No-code NFT lazy-mint widget from buildship.xyz
---

# How to connect Metamask to Webflow

This widget allows minting NFTs on your website.

### Outline

Steps are the following:

Prerequisites:

* Make sure your smart-contract has exported `price` and `mint` methods. The possible naming conventions are: `mint`, `buy` or `mintXXX`; `price` or `cost`.
* Have your Webflow website setup and at least on "Basic" plan (required to add custom code blocks)

Steps Overview:

* Add a new page to your Webflow website
* Add a button with id = "mint-button"
* Create "Embedded HTML code" block
* Paste Webflow snippet to the page
* Update code snipper with your contract address (see below)

### Installation

To start, you need an Ethereum NFT contract. [Contact us to deploy it using Buildship](https://buildship.xyz), or test with an [example contract](https://github.com/buildship-dev/webflow-nft-components#example-for-testing).

**MetaverseNFT** contract by [buildship.xyz](https://buildship.xyz) is used by **40+** collections with **1500ETH+** in total volume. It features **40% lower** mint gas fees, costs **\~100$ in gas to deploy**, bullet-proof security and extensions like presale lists, mint passes, etc.

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

1.  If you **have your Ethereum NFT contract**

    ✅ insert your contract address in `CONTRACT_ADDRESS` field

    ✅ set `IS_TESTNET` to `false` or `true` depending on which network is the contract on: `Ethereum Mainnet` or `Rinkeby Testnet`.

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

If that instruction didn't work, check out our ready-to-use minting website template: https://textapes.art

[Contact us](https://buildship.xyz) to get this Webflow template, or to get help with this widget

### Audio transcript

hey guys

so today i'm gonna show you how to use build ship mint widget with your webflow website

so let's go to google and find how to connect your web3 minting platform with webflow website

so to follow this guide you need a deployed nft contract if you don't have a contract deployed you can go to build ship

and fill in the early access form

it would help everyone to launch but right now we're on closed alpha so we only accept submissions via type form and we launch collections on board them manually we have a no code app that allows everyone to launch our collection

so for now if you already have a contract if you don't have you can use our and open source contracts featuring in this repository

so for your contract you should have to

you should have two methods exported first one is price

and price in the way

you can name it get price or price or cost as long as it's supported by a widget the prices should be invade

so this for example is point one is

another one is

mint the mint metal choose accept payable amount of eth let's say 0.1 and number of tokens you want to mint

that's pretty standard so if you have this you can follow

to webflow let's create a new website

so following the guide we need to create embedded html code block and be right that you have to have the paid basic plan to do that

the custom code we use

should contain your contract address

if you have your contract not verified on etherscan you should paste your contract api here we're gonna not gonna do that

so given that our version is on rinkeby

we used is testnet equals true network id equals four if your contract is on mainnet you don't need to put this

the second thing

you gonna do

we create button with id that says mint button this is important because using this id our script will find the button on your website and allow you to mint

so we go here

and we use mint button

okay now we publish

let's check it out

so when you click it should present you with a build ship widget you can add styling to that

for example

if your website is in dark theme

you can use theme dog

oh

let's publish again

so

if your contract has any error it will present you here for example one of the most frequent errors is sale not started

so

so

me

thank you

so

so we see the transaction has failed because the contract has an error

that's all thank you for watching this video

bye bye

### Formatted version

What should user do to connect their web3 wallet to their webflow website?

* Step 1: Go to [Google](https://www.google.com) and search for how to connect your web3 wallet to your webflow website.
* Step 2: Follow the instructions on the page.
* Step 3: Copy and paste the code below into the custom code field of your website.
* Step 4: Publish your website.

```
{
  "networkId": 4,
  "testnet": true,
  "contractAddress": "0x0"
}
```

* Step 5: Click the "Mint" button on your website.
* Step 6: Enter the amount of ETH you want to send to the contract.

