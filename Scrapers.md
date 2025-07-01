**SCRAPERS**

===============================================

**About**

The setup for scraping the trading data is built around multiple virtual machines accessing endpoints found via official api provieders and random request headers form various trading terminals. 

Each wallet takes two seperate endpoint pull requests to gather all the data. One for general statistics and the other for FDV range insights on trade ranges.

Avoiding rate limiting and 403s with: TLS Client, Headers, Proxy Rotations, Cookie Injections

The scripts are run on Linux Virtual machines; Each network has their own running independent when scraping

Analyzes first 70 traders and the top 100 most profitable traders of trending tokens of the past 1h, 6hr, 12hr, 24hr time frames daily


===============================================

**Basic GUI Example**

![image](https://github.com/user-attachments/assets/f5ad1888-fa3a-4a60-a7ee-9c9ad0121256)

===============================================

**TRADER STATISTICS**

*Below are the stats available for every trader in the database* 

**wallet** *the traders address on the respective blockchain* 

**unrealized_profit** *all time unrealized profit* 

**unrealized_pnl** *all time unrealized pnl percent* 

**realized_profit_7d** *weekly realized profit* 

**realized_profit_30d** *monthly realized profit* 

**total_profit** *all time profit* 

**winrate** *all time winrate percentage for tokens traded* 

**all_pnl** *all time trading pnl percent* 

**buy_7d** *weekly buy transactions*

**sell_7d** *weekly sell transactions* 

**token_sold_avg_profit** *average profit per trade*

**balance** *native balance in wallet respective to the network*

**pnl_lt_2x_num** *number of trades with a minimum 2x gain*

**pnl_2x_5x_num** *number of trades with a range of 2x - 5x return*

**pnl_gt_5x_num** *number of trades with a 5x return or greater*

**tags** *keywords/tags to identify type of trader*

**avg_holding_peroid** *average holding time per trade from time of first buy to first sell*

**sub 75k avg entry** *average market cap entry for coins bought under 75k*

**sub 75k entries** *transactions for coins in this range*

**sub 75k avg buy amount** *average buy amount for transactions in this range*

**sub 75k avg buy 30d** *aveage monthly buy transactions per trade*

**sub 75k avg sell 30d** *aveage monthly sell transactions per trade*

**sub 75k avg total profit pnl** *average pnl percent per trade in this range*

**75k - 250k avg entry** *average market cap entry for coins bought between 75k - 250k*

**75k - 250k entries** *transactions for coins in this range*

**75k - 250k avg buy amount** *average buy amount for transactions in this range*

**75k - 250k avg buy 30d** *aveage monthly buy transactions per trade*

**75k - 250k avg sell 30d** *aveage monthly sell transactions per trade*

**75k - 250k avg total profit pnl** *average pnl percent per trade in this range*

**fast_trades_percentage** *percent of trades that are "fast", considered 60 seconds or under holding time*

**date_reviewed** *last time the wallet was scraped and checked*

===============================================


