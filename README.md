# Efficient Portfolio Construction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SLOCZVNzx8zMBftkt5v8KA3CwtHMlguU?usp=sharing)

This is a Google Colaboratory (Jupyter notebook) implementation of [Robert C. Merton](https://en.wikipedia.org/wiki/Robert_C._Merton)'s efficient portfolio algorithm from the paper *An Analytic Derivation of the Efficient Portfolio Frontier* (1972).

In the paper, Merton identifies an algorithm that, given historical returns data from several identified securities, constructs a portfolio with the <ins>lowest variance in returns for a given level of expected returns</ins> (this is the "efficiency").

The algorithm outputs the fraction of the portfolio to be allocated to each security. Each may be positive or negative corresponding to long and short positions, or zero when no position should be taken. They are guaranteed to sum to 100%.

The linked notebook as written returns such a portfolio using some or all constituents of the S&P 100 index with available returns data from 2010-2019. You must specify the level of expected returns at which to perform the allocation.

**Keep in mind the portfolio is only efficient for time periods with available returns data. The results are not forward-looking, nor are they advice to buy or sell any security.**

Example expected return: `25%`.

|Symbol|Allocation            |
|------|----------------------|
|MRK   |0.3972                |
|AMT   |0.3784                |
|VZ    |0.3203                |
|MO    |0.1772                |
|BRK-B |0.1749                |
|DHR   |0.1717                |
|MCD   |0.1695                |
|SBUX  |0.1449                |
|BMY   |0.1446                |
|ALL   |0.1255                |
|T     |0.1238                |
|UNH   |0.1188                |
|AAPL  |0.1155                |
|BA    |0.1071                |
|HD    |0.0874                |
|WBA   |0.0781                |
|ORCL  |0.0765                |
|C     |0.0656                |
|BLK   |0.0648                |
|EMR   |0.0641                |
|MA    |0.0598                |
|KO    |0.0531                |
|JNJ   |0.0509                |
|BAC   |0.0504                |
|SO    |0.0459                |
|EXC   |0.0428                |
|COF   |0.0400                |
|ABT   |0.0388                |
|UPS   |0.0383                |
|V     |0.0380                |
|DUK   |0.0376                |
|LOW   |0.0288                |
|DD    |0.0278                |
|FDX   |0.0271                |
|NFLX  |0.0237                |
|RTX   |0.0222                |
|AMGN  |0.0217                |
|CVX   |0.0209                |
|CRM   |0.0200                |
|GOOG  |0.0165                |
|MS    |0.0158                |
|PM    |0.0141                |
|ADBE  |0.0134                |
|WFC   |0.0123                |
|OXY   |0.0107                |
|BKNG  |0.0085                |
|TXN   |0.0052                |
|GOOGL |0.0042                |
|QCOM  |0.0004                |
|SLB   |0.0001                |
|PFE   |-0.0053               |
|LMT   |-0.0085               |
|AIG   |-0.0091               |
|BK    |-0.0091               |
|GE    |-0.0098               |
|CMCSA |-0.0101               |
|INTC  |-0.0117               |
|HON   |-0.0170               |
|NEE   |-0.0188               |
|CVS   |-0.0208               |
|GILD  |-0.0237               |
|F     |-0.0243               |
|SPG   |-0.0245               |
|NKE   |-0.0245               |
|AMZN  |-0.0271               |
|MMM   |-0.0295               |
|USB   |-0.0302               |
|GS    |-0.0312               |
|TMO   |-0.0330               |
|TGT   |-0.0341               |
|MSFT  |-0.0348               |
|GM    |-0.0353               |
|CHTR  |-0.0394               |
|UNP   |-0.0410               |
|NVDA  |-0.0422               |
|BIIB  |-0.0504               |
|LLY   |-0.0580               |
|JPM   |-0.0644               |
|WMT   |-0.0663               |
|GD    |-0.0717               |
|MDLZ  |-0.0725               |
|MDT   |-0.0725               |
|MET   |-0.0803               |
|ACN   |-0.0856               |
|CSCO  |-0.1055               |
|PEP   |-0.1060               |
|CL    |-0.1106               |
|PG    |-0.1146               |
|IBM   |-0.1219               |
|COP   |-0.1326               |
|XOM   |-0.1330               |
|CAT   |-0.1393               |
|DIS   |-0.1659               |
|AXP   |-0.1957               |
|COST  |-0.3529               |


If $10,000 was invested with that allocation (and rebalanced monthly) between January 2011 and December 2019 the portfolio would have had the following returns:
<img src="example_analysis/portfolio_growth.png" alt="growth" width="100%"/>
<img src="example_analysis/annual_returns.png" alt="returns" width="100%"/>
<img src="example_analysis/drawdowns.png" alt="drawdowns" width="100%"/>
<img src="example_analysis/summary.png" alt="summary" width="100%"/>
<img src="example_analysis/metrics.png" alt="metrics" width="100%"/>
