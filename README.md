---
cover: .gitbook/assets/Banner_Twitter (3).png
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 🟡 Introduction to Mosaic

Mosaic envisions a world where anyone can trade their funds freely, reliably, and effortlessly on their own terms. Built natively on Movement and grounded in DeFi principles of open access, Mosaic is a DEX Aggregator and DeFi hub that empowers users with the insights and tools to trade without intermediaries. It offers a fast, secure, and user-friendly platform. No matter your path to financial autonomy, Mosaic has you covered.

Whether you are a developer looking to integrate with our platform, a trader seeking to understand our features, or a new user curious about decentralized exchange, you’ve come to the right place. This documentation provides comprehensive guides, detailed API references, and all the resources you need to effectively utilize Mosaic.

### Jump right in

<table data-card-size="large" data-view="cards" data-full-width="false"><thead><tr><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>User Guides</strong></td><td></td><td><a href=".gitbook/assets/User.png">User.png</a></td><td></td><td><a href="broken-reference">Broken link</a></td></tr><tr><td>Products</td><td></td><td><a href=".gitbook/assets/Banner.png">Banner.png</a></td><td></td><td><a href="broken-reference">Broken link</a></td></tr><tr><td><strong>Swap Integration</strong></td><td></td><td><a href=".gitbook/assets/Swap-Integration.png">Swap-Integration.png</a></td><td></td><td><a href="broken-reference">Broken link</a></td></tr><tr><td><strong>Security and License</strong></td><td></td><td><a href=".gitbook/assets/Security-and-License.png">Security-and-License.png</a></td><td></td><td><a href="broken-reference">Broken link</a></td></tr></tbody></table>

### Protocol Fees 
Since 15 Oct, Mosaic Aggregator has been charging protocol fees per swap, taken once at on-chain settlement.

Protocol fee is Fixed by the aggregator and tiered by pair type to align with expected routing complexity and market risk.

| Pair type        | Protocol fee | Fee tier (bps) |
|------------------|-------------:|---------------:|
| Stable           | 0.01%        | 1              |
| Correlated pairs | 0.03%        | 3              |
| Common pairs     | 0.05%        | 5              |
| Others           | 0.10%        | 10             |

<sub>*bps = basis points; 1 bps = 0.01%.*</sub>

#### Collection mechanics

- Single take: Fees are collected once per swap by the settlement contract; underlying DEX pool fees still apply as usual.
- Where fees are taken: Fees can be taken from token in or token out (never both) depending on route constraints and to preserve price integrity.

#### Token Addresses
Full list

| Asset    | Category   | Contract address |
|----------|------------|------------------|
| USDT.e   | Stablecoin | `0x447721a30109c662dde9c73a0c2c9c9c459fb5e5a9c92f03c50fa69737f5d08d` |
| USDC.e   | Stablecoin | `0x83121c9f9b0527d1f056e21a950d6bf3b9e9e2e8353d0e95ccea726713cbea39` |
| USDa     | Stablecoin | `0x48b904a97eafd065ced05168ec44638a63e1e3bcaec49699f6b8dabbd1424650` |
| USDe     | Stablecoin | `0x9d146a4c9472a7e7b0dbc72da0eafb02b54173a956ef22a9fba29756f8661c6c` |
| WBTC.e   | BTC        | `0xb06f29f24dde9c6daeec1f930f14a441a8d6c0fbea590725e88b340af3e1939c` |
| solvBTC  | BTC        | `0x527c43638a6c389a9ad702e7085f31c48223624d5102a5207dfab861f482c46d` |
| LBTC     | BTC        | `0x0658f4ef6f76c8eeffdc06a30946f3f06723a7f9532e2413312b2a612183759c` |
| stBTC    | BTC        | `0x95c0fd13373299ada1b9f09ff62473ab8b3908e6a30011730210c141dffdc990` |
| enzoBTC  | BTC        | `0xff91f0df99b217436229b85ae900a2b67970eda92a88b06eb305949ec9828ed6` |
| WETH.e   | ETH        | `0x908828f4fb0213d4034c3ded1630bbd904e8a3a6bf3c63270887f0b06653a376` |
| ezETH    | ETH        | `0x2f6af255328fe11b88d840d1e367e946ccd16bd7ebddd6ee7e2ef9f7ae0c53ef` |
| rsETH    | ETH        | `0x51ffc9885233adf3dd411078cad57535ed1982013dc82d9d6c433a55f2e0035d` |
| weETH    | ETH        | `0xe956f5062c3b9cba00e82dc775d29acf739ffa1e612e619062423b58afdbf035` |
