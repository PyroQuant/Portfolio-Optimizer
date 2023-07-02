# Portfolio Optimization

This Python script performs portfolio optimization based on different optimization criteria: 'sharpe', 'cvar', 'sortino', and 'variance'. The script uses historical stock price data downloaded from Yahoo Finance.

## Dependencies

The script depends on the following Python libraries:

- numpy
- pandas
- yfinance
- matplotlib
- scipy

## How to use

The script starts by defining the optimization criterion and the stocks to be included in the portfolio. The time period for which the stock price data will be downloaded is also defined.

```python
optimization_criterion = 'cvar'  # Change to 'sharpe', 'cvar', 'sortino', or 'variance' to optimize those criteria
symbols = ['AAPL', 'MSFT', 'GOOG', 'AMZN', 'META']
start_date = '2018-01-01'
end_date = '2023-01-01'
```

Then, the script downloads the stock price data and calculates the daily returns.

Next, the objective functions for each optimization criterion are defined. These functions are used in the optimization process to determine the optimal combination of weights for the stocks in the portfolio.

The script then performs portfolio optimization using the 'SLSQP' (Sequential Least Squares Programming) optimization method from the scipy library.

After optimization, the script calculates and plots the efficient frontier, which shows the possible combinations of return and volatility for different weights of the stocks in the portfolio.

Finally, the script calculates a series of descriptive statistics for the optimized portfolio, including annualized return, annualized volatility, skewness, kurtosis, maximum drawdown, Sharpe ratio, CVaR, Sortino ratio, and variance.

## Results

The script prints the optimal weights for each stock in the portfolio, as well as the descriptive statistics of the portfolio, for each optimization criterion.

![Output Image](https://github.com/PyroQuant/Portfolio-Optimizer/raw/main/output.png)
[Ver salida del script](https://github.com/PyroQuant/Portfolio-Optimizer/raw/main/output.txt)

## Notes

This script assumes that stock returns are log-normal and that investors are risk-averse. The results may not be accurate if these assumptions are not valid.