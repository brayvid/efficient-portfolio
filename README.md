# Efficient Portfolio Construction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SLOCZVNzx8zMBftkt5v8KA3CwtHMlguU?usp=sharing)

This is an implementation of [Robert C. Merton](https://en.wikipedia.org/wiki/Robert_C._Merton)'s efficient portfolio algorithm from the paper [*An Analytic Derivation of the Efficient Portfolio Frontier*](http://www.stat.ucla.edu/~nchristo/statistics_c183_c283/analytic_derivation_frontier.pdf) (1972), written in a Jupyter notebook (Google Colaboratory).

In the paper, Merton describes an algorithm that, given historical returns data from several identified securities, constructs a portfolio with the <ins>lowest variance in returns for a given level of expected returns</ins> (this is the "efficiency").

The algorithm outputs the fraction of the portfolio to be allocated to each security. Each may be positive or negative corresponding to long and short positions, or zero when no position should be taken. They are guaranteed to sum to 100%.

The linked notebook as written returns such a portfolio using some or all constituents of the S&P 100 index with available returns data from 2010-2019. You must specify the level of expected returns at which to perform the allocation.

**Keep in mind the portfolio is only efficient for time periods with available returns data. The results are not forward-looking, nor are they advice to buy or sell any security.**

Example expected return: `25%`.

Time period valid: `Jan 2011` - `Dec 2019`.

|   Long    	|               	|   Less than 1% 	|               	|   Short   	|               	|
|-----------	|---------------	|----------------	|---------------	|-----------	|---------------	|
|   Symbol  	|   Allocation  	|   Symbol       	|   Allocation  	|   Symbol  	|   Allocation  	|
|   MRK     	|   39.7%       	|   BKNG         	|   0.85%       	|   COST    	|   -35.3%      	|
|   AMT     	|   37.8%       	|   TXN          	|   0.52%       	|   AXP     	|   -19.6%      	|
|   VZ      	|   32.0%       	|   GOOGL        	|   0.42%       	|   DIS     	|   -16.6%      	|
|   MO      	|   17.7%       	|   QCOM         	|   0.04%       	|   CAT     	|   -13.9%      	|
|   BRK-B   	|   17.5%       	|   SLB          	|   0.01%       	|   XOM     	|   -13.3%      	|
|   DHR     	|   17.2%       	|   PFE          	|   -0.53%      	|   COP     	|   -13.3%      	|
|   MCD     	|   17.0%       	|   LMT          	|   -0.85%      	|   IBM     	|   -12.2%      	|
|   SBUX    	|   14.5%       	|   AIG          	|   -0.91%      	|   PG      	|   -11.5%      	|
|   BMY     	|   14.5%       	|   BK           	|   -0.91%      	|   CL      	|   -11.1%      	|
|   ALL     	|   12.6%       	|   GE           	|   -0.98%      	|   PEP     	|   -10.6%      	|
|   T       	|   12.4%       	|                	|               	|   CSCO    	|   -10.5%      	|
|   UNH     	|   11.9%       	|                	|               	|   ACN     	|   -8.6%       	|
|   AAPL    	|   11.6%       	|                	|               	|   MET     	|   -8.0%       	|
|   BA      	|   10.7%       	|                	|               	|   MDT     	|   -7.2%       	|
|   HD      	|   8.7%        	|                	|               	|   MDLZ    	|   -7.2%       	|
|   WBA     	|   7.8%        	|                	|               	|   GD      	|   -7.2%       	|
|   ORCL    	|   7.6%        	|                	|               	|   WMT     	|   -6.6%       	|
|   C       	|   6.6%        	|                	|               	|   JPM     	|   -6.4%       	|
|   BLK     	|   6.5%        	|                	|               	|   LLY     	|   -5.8%       	|
|   EMR     	|   6.4%        	|                	|               	|   BIIB    	|   -5.0%       	|
|   MA      	|   6.0%        	|                	|               	|   NVDA    	|   -4.2%       	|
|   KO      	|   5.3%        	|                	|               	|   UNP     	|   -4.1%       	|
|   JNJ     	|   5.1%        	|                	|               	|   CHTR    	|   -3.9%       	|
|   BAC     	|   5.0%        	|                	|               	|   GM      	|   -3.5%       	|
|   SO      	|   4.6%        	|                	|               	|   MSFT    	|   -3.5%       	|
|   EXC     	|   4.3%        	|                	|               	|   TGT     	|   -3.4%       	|
|   COF     	|   4.0%        	|                	|               	|   TMO     	|   -3.3%       	|
|   ABT     	|   3.9%        	|                	|               	|   GS      	|   -3.1%       	|
|   UPS     	|   3.8%        	|                	|               	|   USB     	|   -3.0%       	|
|   V       	|   3.8%        	|                	|               	|   MMM     	|   -2.9%       	|
|   DUK     	|   3.8%        	|                	|               	|   AMZN    	|   -2.7%       	|
|   LOW     	|   2.9%        	|                	|               	|   NKE     	|   -2.5%       	|
|   DD      	|   2.8%        	|                	|               	|   SPG     	|   -2.5%       	|
|   FDX     	|   2.7%        	|                	|               	|   F       	|   -2.4%       	|
|   NFLX    	|   2.4%        	|                	|               	|   GILD    	|   -2.4%       	|
|   RTX     	|   2.2%        	|                	|               	|   CVS     	|   -2.1%       	|
|   AMGN    	|   2.2%        	|                	|               	|   NEE     	|   -1.9%       	|
|   CVX     	|   2.1%        	|                	|               	|   HON     	|   -1.7%       	|
|   CRM     	|   2.0%        	|                	|               	|   INTC    	|   -1.2%       	|
|   GOOG    	|   1.7%        	|                	|               	|   CMCSA   	|   -1.0%       	|
|   MS      	|   1.6%        	|                	|               	|   GE      	|   -1.0%       	|
|   PM      	|   1.4%        	|                	|               	|   BK      	|   -0.9%       	|
|   ADBE    	|   1.3%        	|                	|               	|   AIG     	|   -0.9%       	|
|   WFC     	|   1.2%        	|                	|               	|   LMT     	|   -0.9%       	|
|   OXY     	|   1.1%        	|                	|               	|   PFE     	|   -0.5%       	|
|   Long    	|   388%      	  |   Total        	|   100%         	|   Short   	|   -288%     	  |

If $10,000 had been invested with that allocation and rebalanced monthly between January 2011 and December 2019, the portfolio would have had the following return profile:
<img src="example_analysis/portfolio_growth.png" alt="growth" width="100%"/>
<img src="example_analysis/annual_returns.png" alt="returns" width="100%"/>
<img src="example_analysis/drawdowns.png" alt="drawdowns" width="100%"/>
<img src="example_analysis/summary.png" alt="summary" width="100%"/>
<img src="example_analysis/metrics.png" alt="metrics" width="100%"/>
