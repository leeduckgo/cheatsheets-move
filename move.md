---
title: MOVE-based Chains
category: Web3
layout: 2017/sheet
weight: -1
updated: 2022-08-29
---

### Quick Start(Starcoin)

Start a node & console.
```bash
# 启动一个本地 dev 节点
$ starcoin -n dev
# 启动一个本地 dev 节点的同时打开控制台，-d 参数可以确保每次打开控制台时都保有历史的数据而不是重开
$ mkdir [folder_name]
$ cd [folder_name]
$ pwd
$ starcoin -d [path_to_your_data_folder] -n dev console
```

Connect to `Barnard Testnet` by console.
```bash
$ starcoin --connect ws://barnard.seed.starcoin.org:9870 --local-account-dir ~/.starcoin/barnard/account_vaults console
```

### Console Account Operations(Starcoin)

```bash

# 指定账户获得测试代币
starcoin% dev get-coin [addr] -v 100STC
# 账户列表
starcoin% account list
# 单一账户情况查看
starcoin% account show [addr]
# 创建新账户
starcoin% account create -p [pwd]
# 解锁账户
starcoin% account unlock
# 导出密钥
starcoin% account export [addr]
# 导出有密码的账户的密钥
starcoin% account export -p [pwd] [addr]
```

### Console Contract Operations(Starcoin)

```bash
# 编译合约
% mpm release
# 部署合约
starcoin% dev deploy [path to blob] -s [addr] -b
# 调用合约中的只读函数
starcoin% dev call --function 0x1168e88ffc5cec53b398b42d61885bbb::EthSigVerifier::verify_eth_sig --arg x"90a938f7457df6e8f741264c32697fc52f9a8f867c52dd70713d9d2d472f2e415d9c94148991bbe1f4a1818d1dff09165782749c877f5cf1eff4ef126e55714d1c" --arg x"29c76e6ad8f28bb1004902578fb108c507be341b" --arg x"b453bd4e271eed985cbab8231da609c4ce0a9cf1f763b6c1594e76315510e0f1"
# 调用合约中的写函数（发送交易）
starcoin% account execute-function --function 0x1168e88ffc5cec53b398b42d61885bbb::MyLibraryV5::s_add_book --arg b"web3" --arg b"github.com" -s 0x1168e88ffc5cec53b398b42d61885bbb -b
# 查看资源
starcoin% state get resource [caller_addr] 0x1168e88ffc5cec53b398b42d61885bbb::MyLibraryV3::Book
```

### Quick Start(Aptos)

//TODO