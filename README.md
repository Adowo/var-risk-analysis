# var-risk-analysis

This project looks at downside risk for a few major stocks and commodities using historical market data, focusing mainly on Value-at-Risk (VaR) and Conditional VaR (CVaR). VaR shows what you can lose given a certain confidence level over a period of time, and CVaR shows, if you're below that confidence cutoff, how bad it can get.

Prices are pulled from `yfinance`, then daily returns are used to estimate annual return, volatility, VaR, and CVaR.  
A quick return distribution plot highlights the VaR cutoff and the CVaR region so you can visually see how often bad days occur, and how ugly they get once you cross that threshold.

### Securities Looked at
- SPY (U.S. equities)
- A Gold ETF
- IEFA (international developed)

###Example:  
Daily return distribution with VaR + CVaR highlighted:  
![plot](images/newplot (1).png)
![plot](images/newplot (2).png)


### Portfolio
This code also creates a portfolio of the three assets with equal weights.  
Returns are combined to calculate the overall performance, plus portfolio level VaR/CVaR.  
This helps show how diversification can affect the downside.

> *(insert image)*  
Example:  
Portfolio Plots:  
![plot](images/newplot (3).png)
![plot](images/newplot (4).png)

### Monte Carlo (not added yet)
Monte Carlo simulation is coming next — the idea is to simulate many random return paths based on historical vol + correlation, then estimate VaR/CVaR from that distribution, And then compare that to using hiistorical data but once again thats future plans.

### Code
Everything in one notebook (`VAR.ipynb`).  
Main tools used: pandas, numpy, yfinance, and plotly.
