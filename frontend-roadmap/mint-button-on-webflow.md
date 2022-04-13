---
description: Open-source drop-in Webflow widget
---

# Mint button on Webflow

## Webflow widget

[https://github.com/buildship-dev/webflow-nft-components](https://github.com/buildship-dev/webflow-nft-components)

## Motivation

Check out the google search results for "connect metamask with webflow". It's a SEO goldmine – many people want it, but there's no good solution.

e.g. see this discussion ([https://webflow.com/website/NFT-store-website-with-minting-and-Metamask-connection](https://webflow.com/website/NFT-store-website-with-minting-and-Metamask-connection))

The possibilities are endless, not only NFT mints, but also DEX interfaces, lending platforms, prediction markets, basically anything from web3 sdk, but even easier to launch.

For v3 or v4, I have even envisioned a Excel-style reactive builder for data logic – you have a list of inputs on the left side, and then you can "code" data processing algos that output values into the interface. I can see even how you can build Uniswap DEX using this type of no-code builder.

## Implementation

The widget is a React-based drop-in, users paste and tag and have it connected to their UI.

In Webflow, they have to configure specific ID on the buttons or text output .

They also have some basic availability for styling or custom options. See this piece of README ([https://github.com/buildship-dev/webflow-nft-components/wiki/Mint-button-widget#how-to-style-minting-dialog](https://github.com/buildship-dev/webflow-nft-components/wiki/Mint-button-widget#how-to-style-minting-dialog))

## Roadmap

* fixing bugs with different wallets (e.g. Metamask, slow estimateGas);
* adding MintPass options (pick NFT to mint);
* token-gated content.
