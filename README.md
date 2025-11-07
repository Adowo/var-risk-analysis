# var-risk-analysis

This project looks at downside risk for a few major stocks and commodities using historical market data, focusing mainly on Value-at-Risk (VaR) and Conditional VaR (CVaR).

VaR shows what you can lose given a certain confidence level over a period of time, and CVaR shows — if you’re below that confidence cutoff — how bad it can get.

Prices are pulled from yfinance, then daily returns are used to estimate annual return, volatility, VaR, and CVaR.  
A quick return distribution plot highlights the VaR cutoff and the CVaR region so you can visually see how often bad days occur and how ugly they get once you cross that threshold.

---

## Securities Looked At
- SPY (U.S. equities)
- A Gold ETF
- IEFA (international developed)

### Example  
Daily return distribution with VaR + CVaR highlighted:

![Gold VaR](images/Gold_Var.png)

---

## Portfolio

An equal-weighted portfolio is created using the three assets.  
Portfolio-level return, VaR, and CVaR are computed to show how combining assets affects the downside.

Portfolio Return:

![Portfolio Return](images/Portfolio_Return.png)

Portfolio VaR / CVaR distribution:

![Portfolio VaR](images/Portfolio_Var.png)

---

## Monte Carlo (not added yet)

Monte Carlo simulation is coming next — the idea is to simulate many random return paths based on historical vol + correlation, then estimate VaR/CVaR from that distribution and compare it to the historical approach.
