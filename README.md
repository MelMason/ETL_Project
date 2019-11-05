# ETL_Project - Cryptocurrencies

**Cryptocurrency is an internet-based medium of exchange which uses cryptographical functions to conduct financial transactions. Cryptocurrencies leverage blockchain technology to gain decentralization, transparency, and immutability.
Cryptocurrencies can be sent directly between two parties via the use of private and public keys.  These transfers can be done with minimal processing fees, allowing users to avoid the steep fees charged by traditional financial institutions**


# Project Scope

To extract available trading data on Top 10 Cryptocurrencies from two different scources, perform data wrangling, merge the datasets. Load into the Database and create Tables for each Cryptocurrency. 
Time Frame : 07-01-2017 to 06-30-2019

## Top 10 currencies identified by Market Trend
- Ethereum
- Litecoin
- Bitcoin
- Stellar Lumens
- EOS
- Cardano
- Tron
- Bitcoin Cash
- Binance Coin
- NEO


# Sources
https://min-api.cryptocompare.com/documentation?key=Historical&cat=dataSymbolHistoday

https://coinmetrics.io/data-downloads

# Steps Taken

1. Accessed data from Cryptocompare through API and retrieved  
  - Exchange Volume and
  - Pricing
2. Downloaded Data on all 10 Currencies from coinmetrics as individual csv. Data Exploratory Analysis involves 
  - Reviewing available data
  - Dropping NA's and not required columns
  - Eliminating rows with date range < 07-01-2017 and > 06-30-2019
  - Using Market Cap and Price to compute Market Supply 
    - Market Supply(No.of coins) = Market Cap in USD / Price in USD 
3. Merge the cleaned files with data from CryptoCompare
4. Loaded the Data into Postgres
5. Created Tables for each cryptocurreny and Master tables by Price and Exchange Volume
6. Created a Table for DateTime Id to reference within each of the cryptocurrency table
7. Tested the Table contents using sql query

# Team Members :
Melissa Mason, Emi Babu, Dan Dragone & Malini Murthy

  

