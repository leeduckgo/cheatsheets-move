---
title: MOVE-based Chains
category: Web3
layout: 2017/sheet
weight: -1
updated: 2022-08-29
---
### Aptos: Quick Start

Install Aptos CLI:
<br>
[https://aptos.dev/tools/aptos-cli/install-cli/](https://aptos.dev/tools/aptos-cli/install-cli/)
```
```

### Aptos: Console Account Operations

Use the Aptos CLI:
<br>
[https://aptos.dev/tools/aptos-cli/use-cli/use-aptos-cli](https://aptos.dev/tools/aptos-cli/use-cli/use-aptos-cli)
```bash
# init aptos acct
# recommand to select testnet, you will get faucet automatically.
$ aptos init
# get more faucet
$ aptos account fund-with-faucet --account [acct]
# by alias
$ aptos account fund-with-faucet --account default
# query balance
$ aptos account list --query balance --account default
# list resources
$ aptos account list --query resources --account default
# list account
$ aptos account list
# list modules
$ aptos account list --query modules
# token transfer
$ aptos account transfer --account superuser --amount 100
```

### Aptos: Console Module(Contract) Operations

interact with aptos modules.
<br>
[https://aptos.dev/tutorials/first-move-module](https://aptos.dev/tutorials/first-move-module)

```bash

# compile module
$ aptos move compile --named-addresses hello_blockchain=default
# deploy module
$ aptos move publish --named-addresses hello_blockchain=default
# interact with module
$ aptos move run --function-id 'default::message::set_message' --args 'string:hello, blockchain'
```

### Aptos: Scaffold-Aptos

use scaffold aptos to generate `dApp`.
<br>
[https://github.com/NonceGeek/scaffold-aptos](https://github.com/NonceGeek/scaffold-aptos)
<br>
[https://github.com/NonceGeek/scaffold-aptos-examples](https://github.com/NonceGeek/scaffold-aptos-examples)

```bash
# install
$ yarn
# modify the configuration
$ vim .env.local
# start with dev mode
$ yarn dev
# buidl
$ yarn build
```

## Awesome Aptos projects!

* [MoveDID](https://movedid.build)

[https://movedid.build](https://movedid.build)
<br>
A DID protocol that follows the w3c specification, and is implemented on Aptos.

* ...
