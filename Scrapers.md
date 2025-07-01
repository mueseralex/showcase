**SCRAPERS**

===============================================

**About**

The setup for scraping the trading data is built around multiple virtual machines accessing endpoints found via official api provieders and random request headers form various trading terminals. 

Each wallet takes two seperate endpoint pull requests to gather all the data. One for general statistics and the other for FDV range insights on trade ranges.

Avoiding rate limiting and 403s with: TLS Client, Headers, Proxy Rotations, Cookie Injections
