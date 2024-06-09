# Efficient Portfolio Construction

<a href="https://colab.research.google.com/github/brayvid/efficient-portfolio/blob/main/EfficientPortfolio.ipynb" rel="Open in Colab"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="" /></a>

**This is not  advice to buy or sell any security.**

This is an implementation of Robert C. Merton's efficient portfolio algorithm from the paper [*An Analytic Derivation of the Efficient Portfolio Frontier*](http://www.stat.ucla.edu/~nchristo/statistics_c183_c283/analytic_derivation_frontier.pdf) (1972) written in Google Colab. [Run it here.](https://colab.research.google.com/drive/1SLOCZVNzx8zMBftkt5v8KA3CwtHMlguU?usp=sharing)

Building on the work of Harry Markowitz, Merton describes a way to assign weights to a list of securities to make a portfolio that has the lowest variance in returns for a given level of expected returns, based on historical returns data. Each weight may be positive or negative corresponding to long and short positions, or zero when no position should be taken. They will sum to 100%.

The notebook above finds such a portfolio using all S&P 100 companies. You specify the level of expected returns at which to perform the allocation. If the entire S&P 100 is used as input with data from 1/1/2011 to 12/31/2019, this is the resulting minimum-variance allocation at the 25% expected return level:

| Long   |            | Less than 1% |            | Short  |            |
|--------|------------|--------------|------------|--------|------------|
| Symbol | Allocation | Symbol       | Allocation | Symbol | Allocation |
| MRK    | 39.7%      | BKNG         | 0.85%      | COST   | -35.3%     |
| AMT    | 37.8%      | TXN          | 0.52%      | AXP    | -19.6%     |
| VZ     | 32.0%      | GOOGL        | 0.42%      | DIS    | -16.6%     |
| MO     | 17.7%      | QCOM         | 0.04%      | CAT    | -13.9%     |
| BRK-B  | 17.5%      | SLB          | 0.01%      | XOM    | -13.3%     |
| DHR    | 17.2%      | PFE          | -0.53%     | COP    | -13.3%     |
| MCD    | 17.0%      | LMT          | -0.85%     | IBM    | -12.2%     |
| SBUX   | 14.5%      | AIG          | -0.91%     | PG     | -11.5%     |
| BMY    | 14.5%      | BK           | -0.91%     | CL     | -11.1%     |
| ALL    | 12.6%      | GE           | -0.98%     | PEP    | -10.6%     |
| T      | 12.4%      |              |            | CSCO   | -10.5%     |
| UNH    | 11.9%      |              |            | ACN    | -8.6%      |
| AAPL   | 11.6%      |              |            | MET    | -8.0%      |
| BA     | 10.7%      |              |            | MDT    | -7.2%      |
| HD     | 8.7%       |              |            | MDLZ   | -7.2%      |
| WBA    | 7.8%       |              |            | GD     | -7.2%      |
| ORCL   | 7.6%       |              |            | WMT    | -6.6%      |
| C      | 6.6%       |              |            | JPM    | -6.4%      |
| BLK    | 6.5%       |              |            | LLY    | -5.8%      |
| EMR    | 6.4%       |              |            | BIIB   | -5.0%      |
| MA     | 6.0%       |              |            | NVDA   | -4.2%      |
| KO     | 5.3%       |              |            | UNP    | -4.1%      |
| JNJ    | 5.1%       |              |            | CHTR   | -3.9%      |
| BAC    | 5.0%       |              |            | GM     | -3.5%      |
| SO     | 4.6%       |              |            | MSFT   | -3.5%      |
| EXC    | 4.3%       |              |            | TGT    | -3.4%      |
| COF    | 4.0%       |              |            | TMO    | -3.3%      |
| ABT    | 3.9%       |              |            | GS     | -3.1%      |
| UPS    | 3.8%       |              |            | USB    | -3.0%      |
| V      | 3.8%       |              |            | MMM    | -2.9%      |
| DUK    | 3.8%       |              |            | AMZN   | -2.7%      |
| LOW    | 2.9%       |              |            | NKE    | -2.5%      |
| DD     | 2.8%       |              |            | SPG    | -2.5%      |
| FDX    | 2.7%       |              |            | F      | -2.4%      |
| NFLX   | 2.4%       |              |            | GILD   | -2.4%      |
| RTX    | 2.2%       |              |            | CVS    | -2.1%      |
| AMGN   | 2.2%       |              |            | NEE    | -1.9%      |
| CVX    | 2.1%       |              |            | HON    | -1.7%      |
| CRM    | 2.0%       |              |            | INTC   | -1.2%      |
| GOOG   | 1.7%       |              |            | CMCSA  | -1.0%      |
| MS     | 1.6%       |              |            |        |            |
| PM     | 1.4%       |              |            |        |            |
| ADBE   | 1.3%       |              |            |        |            |
| WFC    | 1.2%       |              |            |        |            |
| OXY    | 1.1%       |              |            |        |            |
| Long   | 390%       | Total        | 100%       | Short  | -290%      |

If $10,000 had been distributed according to the above table on January 1, 2011 and rebalanced monthly, the portfolio would have had the following returns profile 9 years later on January 1, 2020:
</br>
<img src="example/portfolio_growth.png" alt="growth" width="100%"/>
</br>
The Merton-allocated portfolio had an annualized inflation-adjusted growth rate of 19.8%, compared to 14.1% for an equal-weight allocation:
</br>
<img src="example/summary_table.png" alt="summary" width="100%"/>
</br>
It saw an alpha of over 20% and a beta of 0.07, handily surpassing the equal weight portfolio with 3.5% and 0.97 respectively:
</br>
<img src="example/metrics_table.png" alt="metrics" width="100%"/>
