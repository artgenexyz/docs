# Create your MetaverseNFT public minting

**MetaverseNFTFactory** is an amazing tool that allows you to deploy your NFT contract 10x cheaper. Read more:

[https://twitter.com/caffeinum/status/1473164440778407938](https://twitter.com/caffeinum/status/1473164440778407938)

## Using MetaverseNFTFactory to deploy contract

Follow this link to connect to MetaverseNFTFactory via Ethescan: [https://etherscan.io/address/0x5a89282af1ee4b05989fc4b92aed36e2a196884f#writeContract](https://etherscan.io/address/0x5a89282af1ee4b05989fc4b92aed36e2a196884f#writeContract)

Relevant: How to call contract methods via Etherscan?

Another guide: [Metaverse NFT Factory](https://www.notion.so/Metaverse-NFT-Factory-d0c2be4954ca49808cd8c7b55f203885)

### Parameters

startPrice – public sale price, in wei (10^-18 ETH)

maxSupply – total amount of tokens, mint can never go above that

nReserved – reserved for admin – not for sale

maxTokensPerMint – public sale limit per TRANSACTION

royaltyFee = 0 – not used in this version of factory

uri = https://metadata.buildship.dev/api/token/PROJECTSLUG or your IPFS metadata

### Example:
