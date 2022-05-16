---
description: Deploy feature-rich NFT contracts 10x cheaper to Ethereum
---

# 🏭 What is NFTFactory?

**MetaverseNFTFactory** is an amazing tool by [buildship.xyz](https://buildship.xyz) that allows you to deploy your NFT contract to Ethereum 10x cheaper.

{% hint style="info" %}
Create your NFT drop contract without code on [app.buildship.xyz](https://app.buildship.xyz) (using MetaverseNFTFactory)
{% endhint %}

### True ownership with your own contract

You need your own contract for your NFT collection if you want:

* independence of centralized NFT marketplaces like OpenSea, Rarible
* support secondaries on all major NFT marketplaces: OpenSea, LooksRare, Rarible
* decentralized art storage like IPFS
* minting on your own website
* custom primary & secondary sales splits
* custom features: presale lists, mint passes, on-chain art, staking, vesting, etc.
* unique ASCII artist signature

Usually, your own contract requires coding or hiring your own developers, and costs \~**0.5 ETH** to deploy. Also, it might contain security issues that will lead to unrecoverable loss of funds or blocking bugs.&#x20;

That's why we built our MetaverseNFT contract that already helped creators raise more than **1500ETH (\~4.8M$)** without any security issues.

### Super-cheap deployment gas fees

Factory cuts down contract deployment cost to **0.02-0.04 ETH** (**\~60-100$**) instead of and lets you launch large NFT collections (e.g. PFP drops) with minting on your own website.

### 40% lower minting gas fees

We've been able to reduce minting gas fees by using **ERC721** instead of **ERC721Enumerable** standard

`Disclaimer for pros: most of the users don't need Enumerable specific methods. But for those who need methods like`` `**`walletOfOwner()`**`, you can use free Moralis API for fetching the same data`

### Gas-free OpenSea secondary listings

Before listing on sale on any marketplace, every user needs to pay a huge gas fee (**100$+**) to **approve the marketplace** to transfer the NFTs from the users' wallet in case of a successful sale.&#x20;

With Buildship's **MetaverseNFT** contract, users will just list their NFTs for free on OpenSea, which might drive up your floor price & secondary sales volume.

### Feature-rich with extensions

Even more, Factory architecture allows everyone to build & connect Extensions with additional functionality: batch mint, presale, mint pass, on-chain art, dutch auction, delayed claim etc.

[See examples on GitHub here](https://github.com/buildship-dev/nft-contracts/tree/main/contracts/factory/extensions)
