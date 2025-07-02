# Data Scraping Infrastructure

## Overview

The trading data collection infrastructure operates across multiple virtual machines, utilizing official API providers and diverse trading terminal request headers.

### Key Features
- Dual endpoint architecture per wallet:
  - General statistics collection
  - FDV (Fully Diluted Value) range insights
- Daily analysis of:
  - First 70 traders
  - Top 100 most profitable traders
  - Trending tokens across multiple timeframes (1h, 6h, 12h, 24h)

### Anti-Rate Limiting Measures
- TLS Client implementation
- Dynamic header rotation
- Proxy rotation system
- Cookie injection techniques

### Infrastructure
- Linux-based virtual machines
- Independent network-specific scraping instances
- Distributed processing architecture

## GUI Interface

<p align="center">
  <img src="https://github.com/user-attachments/assets/f5ad1888-fa3a-4a60-a7ee-9c9ad0121256" width="70%" />
</p>

## Collected Trader Statistics

### Basic Information
| Metric | Description |
|--------|-------------|
| `wallet` | Trader's blockchain address |
| `balance` | Native network token balance |
| `tags` | Trader type identifiers |
| `date_reviewed` | Last data update timestamp |

### Profit Metrics
| Metric | Description |
|--------|-------------|
| `unrealized_profit` | All-time unrealized profit |
| `unrealized_pnl` | All-time unrealized PNL percentage |
| `realized_profit_7d` | Weekly realized profit |
| `realized_profit_30d` | Monthly realized profit |
| `total_profit` | All-time profit |
| `token_sold_avg_profit` | Average profit per trade |

### Performance Metrics
| Metric | Description |
|--------|-------------|
| `winrate` | All-time token trading success rate |
| `all_pnl` | All-time trading PNL percentage |
| `buy_7d` | Weekly buy transactions |
| `sell_7d` | Weekly sell transactions |
| `avg_holding_peroid` | Average trade holding duration |
| `fast_trades_percentage` | Percentage of trades held under 60 seconds |

### Trade Size Distribution
| Metric | Description |
|--------|-------------|
| `pnl_lt_2x_num` | Trades with minimum 2x gain |
| `pnl_2x_5x_num` | Trades with 2x-5x return |
| `pnl_gt_5x_num` | Trades with 5x+ return |

### Market Cap Range: Sub 75k
| Metric | Description |
|--------|-------------|
| `sub 75k avg entry` | Average entry market cap |
| `sub 75k entries` | Number of transactions |
| `sub 75k avg buy amount` | Average purchase amount |
| `sub 75k avg buy 30d` | Monthly average buys per trade |
| `sub 75k avg sell 30d` | Monthly average sells per trade |
| `sub 75k avg total profit pnl` | Average PNL percentage |

### Market Cap Range: 75k - 250k
| Metric | Description |
|--------|-------------|
| `75k - 250k avg entry` | Average entry market cap |
| `75k - 250k entries` | Number of transactions |
| `75k - 250k avg buy amount` | Average purchase amount |
| `75k - 250k avg buy 30d` | Monthly average buys per trade |
| `75k - 250k avg sell 30d` | Monthly average sells per trade |
| `75k - 250k avg total profit pnl` | Average PNL percentage |
