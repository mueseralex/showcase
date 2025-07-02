# Trading Database Documentation

## Table of Contents
- [Documentation Structure](#documentation-structure)
- [Project Goal](#project-goal)
- [Supported Networks](#supported-networks)
- [Trader Statistics](#trader-statistics)

## Documentation Structure

| File | Description |
|------|-------------|
| `README.md` | Project information and documentation |
| `Scrapers.md` | Web scraper setup information |
| `Databases.md` | Website and database implementation details |

## Project Goal

The trading databases facilitate tracking and copy trading across multiple blockchain networks and launchpads. By analyzing on-chain trader statistics, users can efficiently identify insiders and profitable traders to follow.

### Key Features
- Paywalled access to website/databases
- Discord authentication required
- Custom user session generation
- Real-time data refresh for authorized users

## Supported Networks

### Trading Data Collection
Data is collected from all launchpads within these networks:
- Solana
- Ethereum
- Base
- Binance Smart Chain

### Coin Trading Databases
- Solana
- Tron
- Ethereum
- Base
- Binance Smart Chain
- Hyperliquid

### Perpetual Trading Databases
- Hyperliquid
- Solana

## Trader Statistics

Each trader in the database includes the following metrics:

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
