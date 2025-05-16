# Swap

### Mosaic Swap: DEX Aggregator on Movement

Mosaic is the default DEX Aggregator on the Movement network, designed to consolidate fragmented liquidity and optimize token swaps. Through its smart routing engine, Mosaic finds the most efficient trade paths across Movement’s top decentralized exchanges and AMM protocols, ensuring users receive the best execution with minimal slippage.

#### Overview

* **Function**: Aggregates on-chain liquidity and routes trades to the most favorable execution path
* **Scope**: Connects with all major DEXs and AMM pools on Movement, including Mosaic’s native pools
* **Interface**: User-facing Swap UI + routing SDK/contract interface for integrators

***

#### Why Use a DEX Aggregator?

DEXs allow users to trade assets directly from wallets via liquidity pools. However, liquidity is often fragmented across multiple DEXs, leading to:

* Higher price impact on single pools
* Poor execution prices, especially for large trades
* Time-consuming manual price comparisons

A DEX aggregator solves this by routing trades through the most efficient combination of pools, hops, and protocols — abstracting complexity while improving outcomes.

***

#### Supported DEXs and Pools

Mosaic currently aggregates liquidity across:

* **Mosaic v2 Pools** (Uniswap v2 model)
* **Mosaic Stable Pools** (Curve-style StableSwap AMM)
* **Yuzu Finance (CLMM)**
* **Meridian**
* **RazorDEX**
* **Interest Protocol**
* **Interest Protocol (CLMM)**
* **WarpGate**
* **Liquidswap**

More integrations will be added as the Movement DeFi ecosystem grows.

***

#### Routing Engine: How It Works

Mosaic’s routing engine runs on-chain and executes each trade atomically. It operates through the following core stages:

**1. Quote Aggregation**

* Queries all integrated DEXs for current prices, liquidity, and slippage on the token pair (or intermediary pairs)
* Builds a real-time snapshot of available liquidity across all pools

**2. Route Construction**

* Constructs possible swap paths (direct and multi-hop)
* Scores each route based on:
  * **Net output** (accounting for slippage)
  * **Gas efficiency**
  * **Hop count**
  * **Liquidity robustness**

**3. Trade Execution**

* A single on-chain transaction executes the chosen path
* Powered by Mosaic’s routing contracts:
  * **Atomic execution**: Trade reverts if any leg fails
  * **Modular architecture**: Easily extensible for new DEXs
  * **Gas-optimized**: Batching, pre-approvals, route compression

***

#### Features

| Feature                     | Description                                                                |
| --------------------------- | -------------------------------------------------------------------------- |
| **Best Price Execution**    | Aggregates across all Movement DEXs to find optimal route                  |
| **Reduced Slippage**        | Splits orders across multiple pools for lower price impact                 |
| **Multi-Hop Support**       | Enables complex routes via intermediary tokens to unlock deeper liquidity  |
| **On-Chain, Non-Custodial** | Fully decentralized swap execution from user wallet                        |
| **Composability**           | Contracts and SDKs can be integrated into wallets, yield optimizers, dApps |

***

#### Upcoming Features

| Feature                 | Description                                                                     |
| ----------------------- | ------------------------------------------------------------------------------- |
| **Limit Orders**        | Allows users to set target prices and execute trades only when conditions match |
| **DCA**                 | Automate periodic token buys with optimized routing per interval                |
| **Cross-Chain Routing** | Future upgrade to bring in liquidity from outside Movement (via bridges)        |

#### Developer & Integrator Use Cases

* **Wallets** can integrate Mosaic’s routing API for better swap outcomes
* **Yield Protocols** can use it to rebalance or auto-swap rewards efficiently
* **New dApps** launching on Movement can instantly access deep liquidity by tapping into Mosaic routes

***

#### Contract Access

Mosaic exposes its router and swap logic via verified smart contracts. Integrators can:

* Query route suggestions via off-chain SDK
* Call router contracts with custom token pairs
* Use routing contracts as backend swap engines in their own interfaces

Full contract documentation and SDKs available \[here].

***

#### Conclusion

Mosaic is the trading backbone of the Movement DeFi stack. Whether you're a trader, builder, or liquidity protocol, Mosaic enables efficient, composable, and trustless trade execution — unlocking the full potential of the Movement ecosystem.

For API keys, SDK usage, and integration support, contact the Mosaic team or visit the developer portal \[link].
