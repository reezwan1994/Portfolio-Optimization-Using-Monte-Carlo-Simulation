# Portfolio Optimization using Monte Carlo Simulation
This repository contains a Jupyter Notebook (PortfolioOptimizationUsingMonteCarloSimulation.ipynb) that demonstrates how to perform **Modern Portfolio Theory (MPT)** optimization using the Monte Carlo Simulation technique. The goal is to identify the asset weighting that yields the highest Sharpe Ratio—the optimal trade-off between risk (volatility) and return.
## Project Overview
The project analyzes the historical price data for a basket of stocks to calculate their expected returns, volatility, and correlation. It then runs thousands of simulations to model various possible portfolio allocations and visualizes the Efficient Frontier.
The Efficient Frontier represents the set of optimal portfolios that offer the highest expected return for a given level of risk, or the lowest risk for a given level of expected return.
The notebook identifies two key optimized portfolios:
1. **Maximum Sharpe Ratio Portfolio**: The portfolio with the best risk-adjusted returns.
2. **Minimum Volatility Portfolio**: The portfolio with the lowest overall risk.
## Assets Under Analysis
The analysis in the notebook focuses on a selection of stocks from the Indian National Stock Exchange (NSE) related to the energy/oil sector, utilizing 5 years of historical data.
| Ticker | Company Name |
|:--- | :--- |
| RELIANCE.NS |Reliance Industries Ltd. |
| IOC.NS | Indian Oil Corporation Ltd. |
| BPCL.NS | Bharat Petroleum Corporation Ltd. |
| HINDPETRO.NS | Hindustan Petroleum Corporation Ltd. |
| MRPL.NS | Mangalore Refinery and Petrochemicals Ltd. |
| CHENNPETRO.NS | Chennai Petroleum Corporation Ltd. |
## Methodology
### 1. Data Acquisition and Preprocessing
- Historical adjusted closing prices are fetched using the yfinance library.
- Daily log returns are calculated to normalize the data.
- The annualized mean return and the covariance matrix are computed.
### 2. Monte Carlo Simulation
- The core of the optimization involves running a Monte Carlo simulation that randomly generates thousands of portfolio weight combinations for the selected assets.
- For each combination, the following metrics are calculated:
- **Annualized Portfolio Return**
- **Annualized Portfolio Volatility (Risk)**
- **Sharpe Ratio**

$\text{Sharpe Ratio} = \frac{\text{Portfolio Return} - \text{Risk-Free Rate}}{\text{Portfolio Volatility}}$ 
(A higher Sharpe Ratio indicates better risk-adjusted performance.)
### 3. Optimization
- The simulated results are then analyzed to find the optimal weights that maximize the Sharpe Ratio and minimize volatility.
## Requirements
The notebook requires the following Python libraries:
- pandas
- numpy
- yfinance
- datetime
- scipy (specifically scipy.optimize.minimize)
- matplotlib
- plotly (for interactive visualization)
### Setup Instructions
1. **Clone the repository:**

git clone https://github.com/reezwan1994/Portfolio-Optimization-Using-Monte-Carlo-Simulation.git

cd Portfolio-Optimization-Using-Monte-Carlo-Simulation

2. Install dependencies:
pip install pandas numpy yfinance scipy matplotlib plotly
3. Run the notebook:
Open the PortfolioOptimizationUsingMonteCarloSimulation.ipynb file in a Jupyter environment (Jupyter Lab, Jupyter Notebook, VS Code, etc.) and run all cells sequentially.
## Visualization
The final output is an interactive scatter plot showing all simulated portfolios (Volatility vs. Returns), colored by their Sharpe Ratio. The two optimized points (Max Sharpe Ratio and Min Volatility) are clearly marked on the Efficient Frontier.
