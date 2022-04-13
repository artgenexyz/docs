# How to withdraw the funds via Etherscan?

1. Find your contract address or contract’s Etherscan link (e.g. `etherscan.io/address/0x...`)
2. Go to `Contract` → `Write Contract`, and connect wallet via `Connect to Web3` button
3. Choose **Metamask** or **WalletConnect** (supports Gnosis Multisig or most mobile wallets via QR code)
4. Find `withdraw` function and press `Write`
5. Confirm transaction in your wallet. You can see the status of the transaction on Etherscan or in your wallet.
6. When transaction confirms, the funds will be withdrawed to the contract owner wallet, or the main beneficiary wallet, if set different than the contract’s owner wallet.

> Our fees will be automatically taken on this step. If you have a custom fee split, it will also happen on `withdraw`.
