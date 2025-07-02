# Data Scraping Infrastructure

## Overview

The trading data collection infrastructure operates across multiple virtual machines, utilizing official API providers and diverse trading terminal request headers.

## Flow

graph LR
    subgraph "API Sources"
        A1[Trading APIs]
        A2[Market Data]
        A3[Chain Data]
    end

    subgraph "Network VMs"
        B1[Ethereum VM]
        B2[Solana VM]
        B3[Base VM]
        B4[Tron VM]
        B5[BSC VM]
    end

    subgraph "Processing"
        C1[Git Database]
        C2[Data Validation]
        C3[Stats Processing]
    end

    A1 & A2 & A3 --> B1 & B2 & B3 & B4 & B5
    B1 & B2 & B3 & B4 & B5 --> C1
    C1 --> C2 --> C3
    C3 --> D[Website Interface]

    style A1 fill:#f9f,stroke:#333,stroke-width:2px
    style A2 fill:#f9f,stroke:#333,stroke-width:2px
    style A3 fill:#f9f,stroke:#333,stroke-width:2px
    
    style B1 fill:#bbf,stroke:#333,stroke-width:2px
    style B2 fill:#bbf,stroke:#333,stroke-width:2px
    style B3 fill:#bbf,stroke:#333,stroke-width:2px
    style B4 fill:#bbf,stroke:#333,stroke-width:2px
    style B5 fill:#bbf,stroke:#333,stroke-width:2px
    
    style C1 fill:#bfb,stroke:#333,stroke-width:2px
    style C2 fill:#bfb,stroke:#333,stroke-width:2px
    style C3 fill:#bfb,stroke:#333,stroke-width:2px
    style D fill:#fbb,stroke:#333,stroke-width:2px

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
