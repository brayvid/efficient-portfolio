# Efficient Portfolio Construction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SLOCZVNzx8zMBftkt5v8KA3CwtHMlguU?usp=sharing)

This is a Google Colaboratory (iPython) implementation of [Robert C. Merton](https://en.wikipedia.org/wiki/Robert_C._Merton)'s efficient portfolio algorithm developed in *An Analytic Derivation of the Efficient Portfolio Frontier* (1972).

In the paper, Merton identifies an algorithm which constructs a portfolio from several identified securities, given their historical returns, that has the <ins>smallest variance in returns for a given level of expected returns</ins> (efficient) over the period of the returns data. The algorithm outputs the fraction of the portfolio to be allocated to each. Each of these output percentages may be positive or negative corresponding to long and short positions, or zero when no position should be taken, but they are guaranteed to sum to 100%.

The notebook as written returns a portfolio from some or all constituents of the S&P 100 index with available returns data from 2010-2019.
