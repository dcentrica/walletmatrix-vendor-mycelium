# WalletMatrix

In a nutshell [WalletMatrix](https://walletmatrix.app) is a free-to-use web-based service that provides useful and searchable information about **Bitcoin** wallets and their features. It's aimed at those new and perhaps not so new to the cryptocurrency space, to help find a wallet that suits them.

If you're reading this, then chances are good that you work for a wallet vendor and have been invited and given access to push a JSON file and an optional PGP detached signature to a [Dcentrica](https://dcentrica.com)-owned repository.

# General Procedure

 1. Vendors invited as contributers to a private github repo, via email
 2. Vendors pull the `master` branch and modify the `matrix.json` file
 3. Vendors validate `matrix.json` against the [**WalletMatrix** schema](https://walletmatrix.app/schema/v1.json) and commit changes using GIT
 4. Vendors push changes to the `master` branch
 5. **WalletMatrix** automatically consumes each repo's `matrix.json` file
 6. **WalletMatrix** automatically validates `matrix.json` against a [public schema](https://walletmatrix.app/schema/v1.json).
 7. Vendors that also supply a `matrix.asc` PGP detached signature file, ensures their `matrix.json` files are validated against the signature. If validation fails, data is still imported, but is flagged as "Un-Verified" on **WalletMatrix** itself.

[Find out more here](https://walletmatrix.app/vendors/).

# Requirements

On confirmation of interest, vendors will receive an email with some useful information comprising some of the following:

 1. The URL of the GIT remote to push a `matrix.json` file to.
 2. A one-off UUID that's uses in the `matrix.json` file.
 3. Some basic requirements and additional context such as:

* The email address we use to contact vendors. This should also be associated with the Github account. If the address needs to be changed, just let us know: **hello@dcentrica.com**.
* The email address above is also used as:
  * The primary contact address for inviting wallet vendors to participate
  * The identifier associated with a PGP public key
  * The primary contact address between **WalletMatrix** and wallet vendors
* Vendors will need a valid version 1 JSON file named "matrix.json". This contains structured data about wallet features (See [`the offical v1 JSON Schema`](https://walletmatrix.app/schema/v1.json) and [`an example JSON fle`](./matrix.v1.example.json)) for examples.
* You should optionally provide a detached PGP signature named `matrix.asc` and push that to your private *WalletMatrix** repo alongside your `matrix.json` file
* You should publish a public PGP key associated with the above email address, to a keyserver somewhere. This is consumed by **WalletMatrix** to automatically validate JSON data and can also be used by **WalletMatrix** users to independently validate JSON file contents for themselves
* To update **WalletMatrix** with the latest changes made to your wallet, simply commit your changes to both these files and run:

[Find out more here](https://walletmatrix.app/vendors/).

```shell
    $> git push origin master
```

We suggest you create a dedicated directory on a development environment somewhere where `matrix.json` and `matrix.asc` are generated and maintained.

# FAQ

See the complete list [here](https://walletmatrix.app/vendors).

# Matrix File

See the accompanying [`Wallet JSON Schema`](https://walletmatrix.app/schema/v1.json) and [`matrix.v1.example.json`](./matrix.v1.example.json) files for examples of all supported features, fields and data prototypes.

## Notes

* The name of the features file should be `matrix.json`
* The name of the detached signature file should be `matrix.asc`
* Regular expressions are provided in the official [JSON schema](https://walletmatrix.app/schema/v1.json) to properly structure the data for a given key

