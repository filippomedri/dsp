[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

We use scipy.stats module to generate a normal distribution with mean = 1.78 and standard deviation = 77
```python
import scipy.stats

mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)
```
We evaluate how many people are below 5'10" and  below 6'1" by evaluating the cdf.\
We evaluate than the difference to see how many people are between.

```python
low_than_5_10 = dist.cdf(177.8)    # 5'10"
low_than_6_1 = dist.cdf(185.4)   # 6'1"
between_5_10_and_6_1 = low_than_6_1 - low_than_5_10
low_than_5_10, low_than_6_1, between_5_10_and_6_1
```
(0.48963902786483265, 0.83173371081078573, 0.34209468294595308)

There are about 34% people between 5'10" and 6'1" .