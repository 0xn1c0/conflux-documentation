---
sidebar_position: 1
title: Hardhat 和 Foundry
description: 使用 Hardhat 和 Foundry 部署智能合约
displayed_sidebar: eSpaceSidebar
---

The eSpace Testnet allows anyone to deploy a smart contract on eSpace. In this tutorial, you will learn how to deploy a contract on eSpace Testnet using common tools for developing on Ethereum. This [demo repo](https://github.com/conflux-fans/espace-contract-guide) illustrates contract deployment with [Hardhat](https://hardhat.org/) and [Foundry](https://github.com/foundry-rs/foundry).

在开始部署合约之前，您需要先从[ eSpace 水龙头](https://efaucet.confluxnetwork.org/)获取测试代币。

## 使用 Hardhat 部署智能合约

1. If you haven't already, install [nodejs](https://nodejs.org/en/download/) and [yarn](https://classic.yarnpkg.com/lang/en/docs/install).

2. Clone the repo and install dependencies:

   ```shell
   git clone https://github.com/conflux-fans/espace-contract-guide
   cd espace-contract-guide
   yarn install
   ```

3. Create a `.env` file following the example `.env.example` in the root directory. Change `PRIVATE_KEY` to your own account private key in the `.env`.

4. Run `yarn compile` to compile the contract.

5. Run `yarn deploy:eSpaceTestnet` to deploy the contract on the eSpace Testnet.

6. Run `yarn test` for hardhat tests.

### 视频教程

To learn more about smart contract deployment using Hardhat, please refer to the following videos:

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
<TabItem value="overview" label="Hardhat Overview">
<iframe width="560" height="315" src="https://www.youtube.com/embed/p0Bzc2Y_0Kc?si=sfchFwTtSHlHyK4w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</TabItem>

<TabItem value="tutorial" label="Hardhat Tutorial">
<iframe width="560" height="315" src="https://www.youtube.com/embed/SBzhyV3TSGg?si=HXxu0XdHAsNNJPkf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</TabItem>

</Tabs>

## 使用 Foundry 部署智能合约

1. Clone the repo:

   ```shell
   git clone https://github.com/conflux-fans/espace-contract-guide
   cd espace-contract-guide
   ```

2. Install Foundry:

   ```shell
   curl -L https://foundry.paradigm.xyz | bash
   foundryup
   ```

3. Run `forge build` to build the project.

4. Deploy your contract with Foundry:

   ```bash
   forge create --rpc-url https://evmtestnet.confluxrpc.com \
     --value <lock_amount> \
     --constructor-args <unlock_time> \
     --private-key <your_private_key> \
     --legacy \
     contracts/Lock.sol:Lock
   ```

   - `<lock_amount>` is the amount of test `CFX` to be locked in the contract. Try setting this to some small amount, like `0.0000001ether`.\&#x20
   - `<unlock_time>` is the Unix timestamp after which the funds locked in the contract will become available for withdrawal. Try setting this to some Unix timestamp in the future, like `1730390400` (this Unix timestamp corresponds to October 1, 2024).

   例如：

   ```bash
   forge create --rpc-url https://evmtestnet.confluxrpc.com \
     --value 0.00000000002ether \
     --constructor-args 1696118400 \
     --private-key 0xabc123abc123abc123abc123abc123abc123abc123abc123abc123abc123abc1 \
     --legacy contracts/Lock.sol:Lock
   ```

## 问题和反馈

Thank you for participating in and developing on the eSpace Testnet! 如果您遇到任何问题，请加入我们的 [Discord](https://discord.gg/conflux-network-707952293412339843) 并在其中向我们提问。
