# MetaverseNFTFactory v3 Roadmap

v3 version for Factory should be the state-of-the-art optimized smart-contract, also featuring long-requested updates as:

* ERC721A cheap mints
* Optional unlimited total supply
* Mint by token ID
* Lazy mint: signed and IPFS-stored but unminted NFTs
* OpenZeppelin / Biconomy Relayer (gasless mint [https://portal.thirdweb.com/guides/create-gasless-nft-drop](https://portal.thirdweb.com/guides/create-gasless-nft-drop))
* Refunds/Vesting

## Tasks

**Important**

* [ ] Allow free mint collections to launch without early access pass
* [ ] Implement ERC721A optimization hacks
* [ ] `claimDeveloperFee()` callable by `buildship.eth` wallet
* [ ] LinearVestingExtension
* [ ] MultisigVestingExtension
* [ ] Look into ERC721R for refunds
  * [ ] Build MintRefundExtension?

**Misc**

* [ ] Support for non-transferrable NFTs
* [ ] ASCII art (+ maybe custom contract name)
* [ ] Fix `addExtension()` interface bug (found by sloika)
* [ ] Optional `burn()` method
* [ ] GaslessMintExtension
*   [ ] Hardhat refactor

    [https://github.com/buildship-dev/nft-contracts/pull/39/files](https://github.com/buildship-dev/nft-contracts/pull/39/files)
* [ ] Clean up repo, archive unused contracts and tests
* [ ] Fix CI tests

