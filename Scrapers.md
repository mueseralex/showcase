**SCRAPERS**

===============================================

**About**

The setup for scraping the trading data is built around multiple virtual machines accessing endpoints found via official api provieders and random request headers form various trading terminals. 

Each wallet takes two seperate endpoint pull requests to gather all the data. One for general statistics and the other for FDV range insights on trade ranges.

Avoiding rate limiting and 403s with: TLS Client, Headers, Proxy Rotations, Cookie Injections

The scripts are run on Linux Virtual machines; Each network has their own running independent when scraping

===============================================

**Basic GUI Example**

![image](https://github.com/user-attachments/assets/f5ad1888-fa3a-4a60-a7ee-9c9ad0121256)


