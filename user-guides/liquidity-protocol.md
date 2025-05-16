# Liquidity Protocol

Mosaic’s Liquidity Protocol is a dual-model AMM system built to support both uncorrelated and correlated asset pairs. Designed for simplicity, composability, and capital efficiency, it forms the foundation of Mosaic’s DEX and farming infrastructure on the Movement Network.

#### AMM Architecture

**Uncorrelated Pairs (Constant Product Model)**\
Mosaic supports uncorrelated token pairs using the classic Uniswap v2-style constant product formula (x \* y = k). This model allows passive liquidity provision without active management or complex range settings.

* **Benefits**: Simple LP experience, broad price coverage, proven market model
* **Drawbacks**: Lower capital efficiency, liquidity is spread across the entire price curve, requiring higher TVL to match the depth and slippage performance of concentrated models.

**Correlated Pairs (StableSwap Model)**

For stablecoin pairs and tightly correlated assets (e.g., LSTs), Mosaic implements a **Curve-like StableSwap AMM**. This model reduces slippage in the narrow price ranges where such assets typically trade, making it ideal for efficient swaps between like-valued tokens.

* **Benefits**: Low slippage, improved capital efficiency, ideal for stable or pegged assets
* **Drawbacks**: Not optimal for volatile pairs

Together, these two models create a flexible liquidity layer that adapts to various market needs and asset dynamics on Movement.

***

#### Farming Protocol

Mosaic’s farming module incentivizes LP participation through reward emissions on selected pools. By staking LP tokens, users can earn additional yield in the form of MOVE or other ecosystem incentives.

* **Eligibility**: Only supported pools listed on Mosaic’s farming dashboard
* **Mechanism**: LP tokens are staked into a farming contract, and rewards accumulate over time based on TVL and allocation points
* **Harvesting**: Users can claim rewards at any time, with no lockups or penalties unless otherwise specified

This reward mechanism is designed to bootstrap liquidity and drive deeper market depth across Mosaic’s ecosystem of trading pairs.

***

#### Why Mosaic on Movement?

Mosaic is purpose-built for the Movement Network, inheriting its core advantages:

* **Low Fees**: Movement’s architecture enables near-zero transaction costs, maximizing LP and trader value
* **Non-Custodial & Secure**: All interactions are fully on-chain and self-custodied
* **Composable Ecosystem**: Mosaic’s AMM and farming contracts are modular, enabling future integrations with aggregators, lending protocols, and yield strategies
