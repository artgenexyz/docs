---
description: Self serve no-code NFT collection launcher + custom extensions
---

# app.buildship.xyz

## Self-serve no-code NFT launcher

Demo: [https://unreleased-app.buildship.xyz/](https://unreleased-app.buildship.xyz)

It's closed-source right now; and most probably will be closed.

## Motivation

Users don't know anything about smart-contracts; The only "no-code" alternative is [https://wizard.openzeppelin.com/](https://wizard.openzeppelin.com) + [https://remix.ethereum.org/](https://remix.ethereum.org), which is good enough, but still requires you to suffer a lot. Even me struggles deploying like this.

## Implementation

It's a React dApp, closed-access.

Features:

* deploy NFT smart-contract cheaply to rinkeby or mainnet (+ auto verify on Etherscan);
* upload art to IPFS;
* generate metadata;
* guides to integrate widget into Webflow;
* connect extensions (extension store will come here later).

## Roadmap

* deploy Presale list from CSV (also parse ENS domains);
* adding small features like Opensea royalty config;
* Extension Store – most probably developers of extensions should use web3-sdk and have buildship.json in their repo, which we gonna parse and output extension metadata on this "extensions config" page.
