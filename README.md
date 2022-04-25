# Module_5_Repo

The first part of this project helps the users determine if they have enough money for an emergency fund. The second part of this project creates a financial planner for the user, Using the API Alpaca call to get price data of the stocks and bonds the user needs information on. It also uses the Monte Carlo Simulation to calculate the cumulative return on money for the users in order for them to know if they would be able to retire in either 30 or 10 years depending on their investing portfolio.
---

## Technologies

# This project is written with the programming language python. It also uses the libraries Pandas, alpaca_trade_api, MCSimulation, os, json, dotenv, numpy, and matplot. The project was written on the Windows operating system.
---

## Installation Guide

```
alpaca_api_key = os.getenv("ALPACA_API_KEY")
alpaca_secret_key = os.getenv("ALPACA_SECRET_KEY")
alpaca = tradeapi.REST(
    alpaca_api_key,
    alpaca_secret_key,
    api_version="v2")
```
```
mc_thirty_year = MCSimulation(
    prices_df,
    weights= [.4 , .6],
    num_simulation= 100,
    num_trading_days= 252 * 30
)
```


## Usage

```
start_date = pd.Timestamp("2019-01-24", tz="America/New_York").isoformat()
end_date = pd.Timestamp("2019-04-24", tz="America/New_York").isoformat()
limit_rows = 1000
prices_df = alpaca.get_bars(
    tickers,
    timeframe,
    start = start_date,
    end = end_date
).df
---
prices_df = alpaca.get_bars(
    tickers,
    timeframe,
    start = start_date,
    end = end_date
).df
---

SPY = prices_df[prices_df['symbol']=='SPY'].drop('symbol', axis=1)
AGG = prices_df[prices_df['symbol']=='AGG'].drop('symbol', axis=1)
---



## Contributors


# Creator of this project is Thomas Burns
# Email is burns235577@gmail.com
---