# Protocol Fees

Starting on Oct 15, 2025, swaps on Mosaic include a tiny protocol fee. The fee is set by the Mosaic aggregator and is tiered by pair type. Fees can be taken from either the input token (“token in”) or the output token (“token out”), depending on the route.

### What changes

* A small protocol fee applies to each successful swap on Mosaic.
* Fees are **tiered by pair type** and **fixed by the aggregator**.
* The router continues to optimize for the best executable price after fees.

### How the fee is applied

Mosaic may collect the fee from:

1. **Token in**: a small portion of the input amount is taken before execution, and the remainder is swapped.
2. **Token out**: the full input is swapped, then a small portion of the received output is taken.

The router chooses the collection method that preserves the best executable quote for the user and avoids dust issues.

### Protocol fee tiers

| Pair type        | Fee tier | Fee tier (bps) |
| ---------------- | -------- | -------------- |
| Stable           | 0.01%    | 1              |
| Correlated pairs | 0.03%    | 3              |
| Common pairs     | 0.05%    | 5              |
| Others           | 0.1%     | 10             |

## List of tokens:

### Stables:

<table><thead><tr><th width="98.96875">Token</th><th>Address</th></tr></thead><tbody><tr><td>USDT.e</td><td>0x447721a30109c662dde9c73a0c2c9c9c459fb5e5a9c92f03c50fa69737f5d08d</td></tr><tr><td>USDC.e</td><td>0x83121c9f9b0527d1f056e21a950d6bf3b9e9e2e8353d0e95ccea726713cbea39</td></tr><tr><td>USDa</td><td>0x48b904a97eafd065ced05168ec44638a63e1e3bcaec49699f6b8dabbd1424650</td></tr><tr><td>USDe</td><td>0x9d146a4c9472a7e7b0dbc72da0eafb02b54173a956ef22a9fba29756f8661c6c</td></tr></tbody></table>

### Correlated:

#### BTC

<table><thead><tr><th width="101.0546875">Token</th><th>Address</th></tr></thead><tbody><tr><td>WBTC.e</td><td>0xb06f29f24dde9c6daeec1f930f14a441a8d6c0fbea590725e88b340af3e1939c</td></tr><tr><td>solvBTC</td><td>0x527c43638a6c389a9ad702e7085f31c48223624d5102a5207dfab861f482c46d</td></tr><tr><td>LBTC</td><td>0x0658f4ef6f76c8eeffdc06a30946f3f06723a7f9532e2413312b2a612183759c</td></tr><tr><td>stBTC</td><td>0x95c0fd13373299ada1b9f09ff62473ab8b3908e6a30011730210c141dffdc990</td></tr><tr><td>enzoBTC</td><td>0xff91f0df99b217436229b85ae900a2b67970eda92a88b06eb305949ec9828ed6</td></tr></tbody></table>

#### ETH

<table><thead><tr><th width="104.2734375">Token</th><th>Address</th></tr></thead><tbody><tr><td>WETH.e</td><td>0x908828f4fb0213d4034c3ded1630bbd904e8a3a6bf3c63270887f0b06653a376</td></tr><tr><td>ezETH</td><td>0x2f6af255328fe11b88d840d1e367e946ccd16bd7ebddd6ee7e2ef9f7ae0c53ef</td></tr><tr><td>rsETH</td><td>0x51ffc9885233adf3dd411078cad57535ed1982013dc82d9d6c433a55f2e0035d</td></tr><tr><td>weETH</td><td>0xe956f5062c3b9cba00e82dc775d29acf739ffa1e612e619062423b58afdbf035</td></tr></tbody></table>

### Common

Pairs of MOVE with

<table><thead><tr><th width="101.51171875">Token</th><th>Address</th></tr></thead><tbody><tr><td>USDT.e</td><td>0x447721a30109c662dde9c73a0c2c9c9c459fb5e5a9c92f03c50fa69737f5d08d</td></tr><tr><td>USDC.e</td><td>0x83121c9f9b0527d1f056e21a950d6bf3b9e9e2e8353d0e95ccea726713cbea39</td></tr><tr><td>USDa</td><td>0x48b904a97eafd065ced05168ec44638a63e1e3bcaec49699f6b8dabbd1424650</td></tr><tr><td>USDe</td><td>0x9d146a4c9472a7e7b0dbc72da0eafb02b54173a956ef22a9fba29756f8661c6c</td></tr><tr><td>WBTC.e</td><td>0xb06f29f24dde9c6daeec1f930f14a441a8d6c0fbea590725e88b340af3e1939c</td></tr><tr><td>WETH.e</td><td>0x908828f4fb0213d4034c3ded1630bbd904e8a3a6bf3c63270887f0b06653a376</td></tr></tbody></table>
