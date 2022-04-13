# Configure Whitelist Minting

‼️ You need to have NFT minting deployed to add whitelist! If you don’t have it yet, deploy it following this guide and then have it’s address handy \[Create your MetaverseNFT public minting]\(Create%20you%208b458.md)

## Overview

1. Deploy Whitelist contract and save its address
2. On the `MetaverseNFT` contract, call `addExtension` with `WhitelistSaleExtension` address.
3. Call `updateStartTimestamp` with date from [https://www.unixtimestamp.com/](https://www.unixtimestamp.com)
   1. Optionally, directly `startSale` from the contract
4. Collect your list of addresses as csv and send them to us (later this step will be automated)
   1. We give you a merkle root of the new list, and whitelist ID.
5. Push whitelistRoot via `updateWhitelistRoot`
6. Add embed to your website: [https://github.com/buildship-dev/webflow-nft-components/tree/feature/whitelist/mint-whitelist#how-to-use](https://github.com/buildship-dev/webflow-nft-components/tree/feature/whitelist/mint-whitelist#how-to-use)
7. Your sale is ready and live on your website!

Relevant: How to call contract methods via Etherscan?

## Deploying Whitelist contract

You NEED to have your `MetaverseNFT` sale contract address ready. Please replace it in this link, and then run the link:

[https://gate.buildship.dev/deploy/bafkreiauugtl64cembsruezrux5ljedy5jpto5uviol666wxxbaclyf4he?args=\["0xYOURADDRESS","0x0",0,1\]](https://gate.buildship.dev/deploy/bafkreiauugtl64cembsruezrux5ljedy5jpto5uviol666wxxbaclyf4he?args=%5B%220xYOURADDRESS%22,%220x0%22,0,1%5D)

```jsx
https://gate.buildship.dev/deploy/bafkreiauugtl64cembsruezrux5ljedy5jpto5uviol666wxxbaclyf4he?args=%5B%220xYOURADDRESS%22,%220x0%22,0,1%5D
```

‼️ Try Testnet version first if you’re not confident!

[https://gate-rinkeby.buildship.dev/deploy/bafkreiauugtl64cembsruezrux5ljedy5jpto5uviol666wxxbaclyf4he?args=\["0xYOURADDRESS","0x0",0,1\]](https://gate-rinkeby.buildship.dev/deploy/bafkreiauugtl64cembsruezrux5ljedy5jpto5uviol666wxxbaclyf4he?args=%5B%220xYOURADDRESS%22,%220x0%22,0,1%5D)

Relevant: Deploying MetaverseNFT public sale Create your MetaverseNFT public minting
