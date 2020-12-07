# Efficient Portfolio Construction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SLOCZVNzx8zMBftkt5v8KA3CwtHMlguU?usp=sharing)

This is a Google Colaboratory (Jupyter notebook) implementation of [Robert C. Merton](https://en.wikipedia.org/wiki/Robert_C._Merton)'s efficient portfolio algorithm from the paper *An Analytic Derivation of the Efficient Portfolio Frontier* (1972).

In the paper, Merton identifies an algorithm that, given historical returns data from several identified securities, constructs a portfolio with the <ins>lowest variance in returns for a given level of expected returns</ins> (this is the "efficiency").

The algorithm outputs the fraction of the portfolio to be allocated to each security. Each may be positive or negative corresponding to long and short positions, or zero when no position should be taken. They are guaranteed to sum to 100%.

The linked notebook as written returns such a portfolio using some or all constituents of the S&P 100 index with available returns data from 2010-2019. You must specify the level of expected returns at which to perform the allocation.

**Keep in mind the portfolio is only efficient for time periods with available returns data. The results are not forward-looking, nor are they advice to buy or sell any security.**

`Assumed total annual return: 25.0%.`

|Symbol|Allocation            |
|------|----------------------|
|MRK   |0.3972205589675351    |
|AMT   |0.3783582015900351    |
|VZ    |0.3202755681815359    |
|MO    |0.17719959972344493   |
|BRK-B |0.17489104839248878   |
|DHR   |0.17166311623311303   |
|MCD   |0.1695267146573016    |
|SBUX  |0.14487804294051074   |
|BMY   |0.14456564883440723   |
|ALL   |0.1254830921837608    |
|T     |0.12381110309592498   |
|UNH   |0.11876206339787432   |
|AAPL  |0.11554665742437792   |
|BA    |0.1070973683046192    |
|HD    |0.08744036923946771   |
|WBA   |0.07805052817126512   |
|ORCL  |0.07647133286952344   |
|C     |0.06556643092689206   |
|BLK   |0.06481346047814728   |
|EMR   |0.0641065221792536    |
|MA    |0.0598243414974364    |
|KO    |0.0530697615890368    |
|JNJ   |0.050904068468530746  |
|BAC   |0.05038378198704709   |
|SO    |0.04593382834708014   |
|EXC   |0.04278802712372627   |
|COF   |0.04003970314495756   |
|ABT   |0.03882685559832878   |
|UPS   |0.0382897758819761    |
|V     |0.03801780283146782   |
|DUK   |0.03757396127344294   |
|LOW   |0.02882480577157561   |
|DD    |0.027829993974072945  |
|FDX   |0.02710178421951142   |
|NFLX  |0.02367988443825572   |
|RTX   |0.02222686861321084   |
|AMGN  |0.021666740569665378  |
|CVX   |0.020   |
|CRM   |0.020   |
|GOOG  |0.016   |
|MS    |0.015   |
|PM    |0.014   |
|ADBE  |0.013   |
|WFC   |0.012   |
|OXY   |0.010   |
|BKNG  |0.008   |
|TXN   |0.005   |
|GOOGL |0.004   |
|QCOM  |0.000   |
|SLB   |0.000   |
|PFE   |-0.005  |
|LMT   |-0.008  |
|AIG   |-0.009  |
|BK    |-0.009  |
|GE    |-0.009  |
|CMCSA |-0.010  |
|INTC  |-0.011  |
|HON   |-0.017  |
|NEE   |-0.018  |
|CVS   |-0.020  |
|GILD  |-0.023  |
|F     |-0.024  |
|SPG   |-0.024  |
|NKE   |-0.024  |
|AMZN  |-0.027  |
|MMM   |-0.029  |
|USB   |-0.030  |
|GS    |-0.031  |
|TMO   |-0.032  |
|TGT   |-0.034  |
|MSFT  |-0.034  |
|GM    |-0.035  |
|CHTR  |-0.039  |
|UNP   |-0.040  |
|NVDA  |-0.042  |
|BIIB  |-0.050  |
|LLY   |-0.058  |
|JPM   |-0.064  |
|WMT   |-0.066  |
|GD    |-0.071  |
|MDLZ  |-0.072  |
|MDT   |-0.072  |
|MET   |-0.080  |
|ACN   |-0.085  |
|CSCO  |-0.105  |
|PEP   |-0.106  |
|CL    |-0.110  |
|PG    |-0.114  |
|IBM   |-0.121  |
|COP   |-0.132  |
|XOM   |-0.132  |
|CAT   |-0.139  |
|DIS   |-0.165  |
|AXP   |-0.195  |
|COST  |-0.352  |

If $10,000 was invested with that allocation (and rebalanced monthly) between January 2011 and December 2019 the portfolio would have had the following returns:
<img src="example_analysis/portfolio_growth.png" alt="growth" width="100%"/>
<img src="example_analysis/annual_returns.png" alt="returns" width="100%"/>
<img src="example_analysis/drawdowns.png" alt="drawdowns" width="100%"/>
<img src="example_analysis/summary.png" alt="summary" width="100%"/>
<img src="example_analysis/metrics.png" alt="metrics" width="100%"/>
