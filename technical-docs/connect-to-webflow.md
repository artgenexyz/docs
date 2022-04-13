# Connect to Webflow

‼️ You need to have NFT smart-contract deployed! If you don’t have it yet, follow this guide: \[Create your MetaverseNFT public minting]\(Create%20you%208b458.md)

Webflow connection is very easy! Basically all you need is add Webflow Embed block. Follow this guide:

[https://github.com/buildship-dev/webflow-nft-components/tree/main/mint](https://github.com/buildship-dev/webflow-nft-components/tree/main/mint)

```html
<script>
   CONTRACT_ADDRESS = "<your contract address here>"
   NETWORK_ID = 1
   MAX_PER_MINT = 20
</script>
<script src="https://nftcomponents.vercel.app/static/js/main.js"></script>
<link href="https://nftcomponents.vercel.app/static/css/main.css" rel="stylesheet">
```

‼️ If you need to connect your whitelist to Webflow, the guide is a bit different. You need to setup a button with \`mint-whitelist\` ID and call \`addExtension\` on Etherscan: \[Configure Whitelist Minting]\(Configure%20%20cc9aa.md)

## Example

Check out example integration: [https://textapes.art/](https://textapes.art). The result should be like this:

![https://github.com/buildship-dev/webflow-nft-components/raw/main/public/images/screenshot.png](https://github.com/buildship-dev/webflow-nft-components/raw/main/public/images/screenshot.png)
