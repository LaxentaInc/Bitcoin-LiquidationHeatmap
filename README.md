### Liquidation Heatmaps for BTCUSDT, derived from MultiExchange engines, to cover around 94%+ Liquidity.
one could js ask for the binary if they see this early,  else i will upload it soon enough anyways
!! Liquidity heatmaps are predictive in nature, it decides the direction, not how long the liquidations will last, and is not accurate to the exact prices.
So this will give you uhhh:
- handling of raw network payloads from 8 derivatives exchanges to aggregate a raw, unfiltered global liquidity In **TRILLIONS**.
- Spatial Binning Maps forced leverage cascades and resting order depth into high-resolution price bins, identifying macro shelves and squeeze targets down to r= 0.0400 ish.
- Coinglass or Kraken etc. HEAVILY Charge like **600-999** dollars for liquidations, Like i am not kidding, you could go see yourself! They do not provide liquidation heat maps in any plan below 699$ (this is not against any company nor i am discouraging to use them, i am just stating facts)

- <img width="1532" height="849" alt="image" src="https://github.com/user-attachments/assets/359be75f-ca94-4fb3-8c38-94b7fb1675c6" />

<img width="1186" height="1040" alt="image" src="https://github.com/user-attachments/assets/e524e4fc-4997-46bf-b2ee-af79dfcd7f4f" />

Sounds like a lie? ehhh nah it is not, made it for my own project, cz who knows when they fix thier api?
<img width="1083" height="716" alt="image" src="https://github.com/user-attachments/assets/2514ad1b-6e10-44ff-869b-1b271b21455a" />


# Quantitative Liquidation Landscape Analysis

- **active timeframe**: 4H
- **reference price**: $86,118
- **timestamp**: Tue, 22 Sep 2026 13:36:22 UTC

## 1. Mai 8-Exchange Aggregated Composite (`liquidation_analysis_composite.json`)

### top resting short liquidation walls (overhead magnets)

| price (usd) | volume (usd m) | distance | direction |
| :--- | :--- | :--- | :--- |
| $87,474.7 | $319.4M | +1.58% | short liquidation |
| $86,986.3 | $252.4M | +1.01% | short liquidation |
| $87,181.6 | $208.9M | +1.24% | short liquidation |

### top resting long liquidation walls (downside shelves)

| price (usd) | volume (usd m) | distance | direction |
| :--- | :--- | :--- | :--- |
| $74,777.6 | $471.5M | -13.17% | long liquidation |
| $79,954.1 | $443M | -7.16% | long liquidation |
| $79,758.7 | $407.2M | -7.38% | long liquidation |
| $74,972.9 | $370.8M | -12.94% | long liquidation |
| $79,172.7 | $324.5M | -8.06% | long liquidation |

### horizon asymmetry distribution

- **scalp horizon (1.5%)**: short $2285.6M vs long $2145.3M (ratio: 1.07, assumption: `balanced_distribution`)
- **intraday horizon (3.0%)**: short $4056.8M vs long $4892.8M (ratio: 0.83, assumption: `balanced_distribution`)
- **swing horizon (5.0%)**: short $4107.6M vs long $6896.4M (ratio: 0.6, assumption: `heavier_long_liquidity`)

## 2. CoinGlass Benchmark Matrix (`liquidation_analysis_coinglass.json`) Binance perps only. Not multi exhcange, could differ in volume.

### top resting short liquidation walls (overhead magnets)

| price (usd) | volume (usd m) | distance | direction |
| :--- | :--- | :--- | :--- |
| $87,318.3 | $66.3M | +1.39% | short liquidation |
| $86,480.8 | $66.3M | +0.42% | short liquidation |
| $86,794.8 | $55M | +0.79% | short liquidation |
| $87,632.4 | $42.3M | +1.76% | short liquidation |

### top resting long liquidation walls (downside shelves)

| price (usd) | volume (usd m) | distance | direction |
| :--- | :--- | :--- | :--- |
| $79,885.3 | $119.7M | -7.24% | long liquidation |
| $84,282.3 | $104.3M | -2.13% | long liquidation |
| $74,755.5 | $99.6M | -13.19% | long liquidation |
| $79,466.5 | $92.9M | -7.72% | long liquidation |
| $85,852.6 | $82.5M | -0.31% | long liquidation |

### horizon asymmetry distribution

- **scalp horizon (1.5%)**: short $461.2M vs long $425.5M (ratio: 1.08, assumption: `balanced_distribution`)
- **intraday horizon (3.0%)**: short $654.2M vs long $1062.1M (ratio: 0.62, assumption: `heavier_long_liquidity`)
- **swing horizon (5.0%)**: short $768.4M vs long $1535.3M (ratio: 0.5, assumption: `heavier_long_liquidity`)

## 3. Binance Single-Exchange Landscape (`liquidation_analysis_binance.json`)

- **primary binance short magnet**: $87474.7 ($121.5M, +1.58%)
- **primary binance long shelf**: $74777.6 ($179.3M, -13.17%)

## 4. Synthesis & Comparative Summary

Sovereign 8-Exchange Aggregated: Nearest short magnet at $87474.7 ($319.4M), nearest long magnet at $74777.6 ($471.5M). CoinGlass Benchmark: Upper magnet at $87318.3 ($66.3M), lower magnet at $79885.3 ($119.7M).

