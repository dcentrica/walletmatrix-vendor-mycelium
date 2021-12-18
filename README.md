# WalletMatrix

[WalletMatrix](https://walletmatrix.app) is a free-to-use web-based service that provides useful and searchable information about **Bitcoin** wallets and their features. It's aimed at those new and perhaps not so new to the cryptocurrency space, to help find a wallet that suits them.

If you're reading this, then chances are good that you work for a wallet vendor, maybe even the vendor for this specific wallet. If so [Let's talk!](https://walletmatrix.app/vendors).

# Requirements

* Your wallet has a repo or repos hosted on github
* As a vendor, you host and maintain a JSON file in your wallet's public github repository
* You (or your devs) can use git
* You (or your devs) are willing to _maintain_ your `matrix.json` wenevr new features are released into you wallet

[See here](https://walletmatrix.app/vendors/).

# FAQ

See the complete list [here](https://walletmatrix.app/vendors).

# Matrix File

See the accompanying [`Wallet JSON Schema`](https://walletmatrix.app/schema) and example [`matrix.json`](https://github.com/dcentrica/walletmatrix-acme-wallet/blob/master/matrix.json) files for examples of all supported features, fields and data prototypes.

## Notes

* The name of the features file should be `matrix.json`
* The name of the detached signature file should be `matrix.asc` (if supplied)
* Regular expressions are provided in the official [JSON schema](https://walletmatrix.app/schema) to properly structure the data for a given key

