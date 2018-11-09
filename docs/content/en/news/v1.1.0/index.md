---
title: eosc v1.1.0 Release
linktitle: eosc v1.1.0 Release
description: Release of eosc v1.1.0
date: 2018-11-08
publishdate: 2018-11-08
lastmod: 2018-11-08
keywords: []
weight: 40
sections_weight: 40
draft: false
aliases: []
toc: false
categories: [blog]
---

With the rapid changes of the EOS mainnet, and the needs of the users and developers of this ecosystem
changing with it, we at EOS Canada are constantly adding more features and functionalities to `eosc`.

We have just released the newest version, v1.1.0. The changes to note are:

* Substantially better layout of `get account` (Thanks to community contribution)
* Added `tools names` to ease in conversion between EOS representation of names, uint, hex, etc...
* Added `tx id` to print the transaction ID of a given transaction .json file.
* Added support for the `EOSC_GLOBAL_INSECURE_VAULT_PASSPHRASE` environment variable, to unlock a vault programmatically. This is very useful for tests. See [eosio.forum](https://github.com/eaoscanada/eosio.forum/blob/da00f31b6c23da46364af912a01990b62a398785/README.md#environment) as an example use case!
* Added a new global flag `-H` / `--http-header` which allows to pass custom arbitrary HTTP headers when performing calls to any API
* This is useful to support certain new, optional features of certain augmented endpoints (such as push guarantee semantics offered by the [dfuse API](https://dfuse.io/)!)
* Added new flag to `tx create`, `-f` / `--force-unique` which allows for quick repeated transactions with same payload (for instance transfers of same value that could not otherwise appear in same block due to `TaPOS` replay protection)
* Added `get scheduled-transactions` which shows transactions that are living in memory on nodes, waiting for eventual execution
* Support eosio.forum referendums:
   * Added `forum list`
   * Adapted `forum propose` to latest release
* Added alias for `tx cancel`, as `system canceldelay` for increased discoverability
* Updated `--sudo-wrap` to use new official name for contract (`eosio.wrap`)   

We are constantly looking for feedback for what features and tools you would like to have available to build dApps on EOS. Please feel free to fork and contribute, and reach out to us in our [Telegram Channel](https://t.me/eoscanada). We look forward to building up the developer toolkit for EOS with the community, and for the community.