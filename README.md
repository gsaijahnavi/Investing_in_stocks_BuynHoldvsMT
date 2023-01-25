# Investing for Stocks (Buy-and-Hold versus Momentum trading using MPT)
 Final Project Video: https://drive.google.com/drive/folders/1G98FXmLlHdMGrq2CxjmHRR5AoDQK6qAy?usp=share_link

### Problem Statement
In this project, the objective is to create a portfolio of stocks that appropriately balances the conflicting risk and profit and compare different investment strategies.

Cleaned Data and performed Exploratory Data Analysis
Peformed MPT, where our goal is to allocate money into stocks to maximize the expected return while accounting risk tolerance, with added constraints
Performed MT on selected portfolio (from MPT) to identify the best strategy for each stock based on the crossing points of the moving average.
Analysis on how our portfolio performed for 100K investment using different strategies.
### SECTORS:

Financials Sector
Materials Sector
Consumer Discretionary Sector
### STOCKS CHOSEN:

Financial Sector (GS, JPM, SCHW)
Materials Sector (LYB, DD, MOS)
Consumer Discretionary Sector (CMG, DPZ, AMZN)

### Portfolio allocation using Non-linear Optimation
![image](https://user-images.githubusercontent.com/82319213/214487436-b200589c-d2c1-4a7c-87f4-01378b25e331.png)

The graph above shows the optimal allocation of stocks at each risk level (x-axis). On the lefthand side, we have low risk and high diversity.
On the righthand side, we have high risk and low diversity. Our efficient frontier is the DPZ stock.

Next we will take a look at risk (X) vs. return (Y) of the efficient frontliner.

### Efficient Frontier

![image](https://user-images.githubusercontent.com/82319213/214487534-be7ccecc-3b5e-4e79-9572-9b6bde89361d.png)

Efficient Frontliner: comprises investment portfolios that offer the highest expected return for a specific level of risk.
With the efficient frontliner, we can see that at a certain point, taking on more risk doesn't increase our returns proportionately. This occurs at ~Risk = 0.00021 which achieves a max return around 0.10%. After this point, for every added unit of return, we are taking more risk (Slope <45 degrees)

## Momentum Trading
In next part of project, we will be picking the three stocks - DPZ, JPM, and DD and evaluate whether momentum trading can generate better portfolio returns than buy and hold. Here we are considering "long" only trades and not trying to make money while shorting of stocks. We use multiple pairs of moving day averages and find out best possible (accurately predicts future price movement and thereby generates high returns) combination of trading days to generate buy/sell signal.

Used below pairs
10 days - 20 days
10 days - 50 days
10 days - 100 days
20 days - 50 days
50 days - 100 days

Best pair is which gives maximum return
For DPZ MT with trading days 10-20 days is giving maximum return.
For JPM MT with trading days 20-50 days is giving maximum return.
For DD MT with trading days 10-20 days is giving maximum return.


## Final results and conclusion

### COMMENTS ON BUY & HOLD vs MOMENTUM TRADING
We are losing less money in momentum trading. This is understandable as we were able to exit positions on DPZ and DD in time to prevent capital erosion. Both these strategies have shorter time frame than JPM momentum trading. In a bull market, JPM may provide better returns than the other two.


### Comparing three strategies
Best Performing Portfolio - S&P 500 Returns of S&P 500: -19.7%
Worst Performing Portfolio - Buy and Hold Strategy Returns of Buy & Hold Strategy: -36.6%
2nd Best Performing Portfolio - Momentum Trading with different trading pairs Return for Momentum Trading - -19.9%
While momentum trading and Buy & Hold in S&P 500 is almost similar in returns. Given the overall transaction costs associated with momentum trading, it may have been much more advantageous to invest in S&P 500 for the year 2022.

### Conclusion
* Strategies for Buy & Hold require much more fundamental assessment of business before shortlisting the stocks.

* Momentum trading strategy can work in bull market when the system is designed to trade only in "long" position. If system were to trade in "short" position, the return for the portfolios of momentum trading may have been very different.

* Adding sophistication to momentum trading strategies such as "Stop Prices" or "Profit Booking" can help reduce the portfolio risk further but can also limit portfolio upsides.

* Momentum strategies are suspectible to time frames - big realization! Shorter timeframes can work when there is volatility in the stock markets. If we were to implement this in real world, we would prefer to use much shorter time frame for bear market and highly volatile market conditions depending on how the "VIX" index is performing and positioned.

* Visualizing the buy and sell signals have helped see the strategy & signals in action.

* Our portfolio still had too much risk concentrated towards one stock. Ideally, we should limit exposure to one stock below 50% to have a well diversified portfolio.

* Analysis of Covariance is an important means to find out stocks that can aid in portfolio diversification.
