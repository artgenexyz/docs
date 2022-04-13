# Web3 SDK

## Web3 SDK

it's a open-source React UI Kit that allows anyone to build web3 apps without prior web3 knowledge.

## Motivation

The premise is that on a top level, developer doesn't need to know about gas, transactions, smart-contract – we can have good defaults that work for any wallet and that provide good UI/UX and feedback.

Developer's job is building UI in React, web3-sdk handles all the rest. Developer only decides which data to take from inputs, which transactions to create on each button click – and every blockchain detail is handled by us; or presented to end user to decide.

## Implementation

As input, the SDK receives only the list of smart-contract addresses used in the app ; and a few API keys: Etherscan, Infura, Alchemy (optional), Onboard.js, Buildship (later when we're bigger).

On build step, the ABIs are fetched from etherscan or from our backend (see this endpoint used in widget [https://metadata.buildship.dev/api/info/0xFdf7BA4Edcb8F3F666239EBdA387506B3c598BD5?network\_id=1](https://metadata.buildship.dev/api/info/0xFdf7BA4Edcb8F3F666239EBdA387506B3c598BD5?network\_id=1) ).

## Drafts

[https://github.com/caffeinum/web3-ui](https://github.com/caffeinum/web3-ui)[https://github.com/buildship-dev/web3-login](https://github.com/buildship-dev/web3-login)

## Reference

[https://github.com/thirdweb-dev/react](https://github.com/thirdweb-dev/react)

## Roadmap

* make it work!
* gather some developer feedback;
* move from onboard.js to wagmi;
* use hooks everywhere;
* web3-login vs. web3-ui React component lib;
* implement build step thing so abstract away "smart-contracts" for the developer;
* transaction handling (popups, see pending txs, retry, re-fetch tx status);
* allow using [thegraph.com](http://thegraph.com) or our backend to make blockchain read requests faster (cache and combine multiple into one);
* non-React integrations: e.g. phaser.js;
* ENS support, NFT avatar support;
* all the fun stuff.
