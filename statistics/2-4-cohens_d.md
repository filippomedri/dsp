[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

First, we evaluate the mean weight of first babies and others babies.

```python
firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()
```
(7.201094430437772, 7.325855614973262) \
It seems that first babies are lighter than others babies.
\
We than evaluate the Cohen Effect Size

```python
difference_in_babies_weight = CohenEffectSize(firsts.totalwgt_lb,others.totalwgt_lb)
difference_in_babies_weight
```
-0.08867292707260174 
\
The effect size is bigger in amplitude than the difference in pregnancy length, but it is still small. \
By the means of both evaluation we can conclude that first babies have both a very small tendency of being lighter and being born later than others.