# Efficient Portfolio Construction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SLOCZVNzx8zMBftkt5v8KA3CwtHMlguU?usp=sharing)

This is a Google Colaboratory (iPython) implementation of [Robert C. Merton](https://en.wikipedia.org/wiki/Robert_C._Merton)'s efficient portfolio algorithm from *An Analytic Derivation of the Efficient Portfolio Frontier* (1972).

In the paper, Merton identifies an algorithm that, given historical returns data from several identified securities, constructs a portfolio with the <ins>lowest variance in returns for a given level of expected returns</ins> (this is the "efficiency").

The algorithm outputs the fraction of the portfolio to be allocated to each. Each of these output percentages may be positive or negative corresponding to long and short positions, or zero when no position should be taken, but they are guaranteed to sum to 100%.

The linked notebook as written returns such a portfolio from some or all constituents of the S&P 100 index with available returns data from 2010-2019. You must specify the level of expected returns as desired.
