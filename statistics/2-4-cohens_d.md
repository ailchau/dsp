[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Excercise 2.4.
Using the variable `totalwgt_lb`, investigate whether first babies are lighter or heavier than others. Compute Cohen's d to quantify the difference between the groups. How does it compare to the difference in preganancy length?

>> The difference in mean total weight between first borns and others is about -0.089 standard deviations, which is arelatively small difference. But it is larger when compared to the effect size of the difference in pregnancy length (i.e., 0.029).

```python
import numpy as np
import nsfg

preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

# calculation of Cohen's d
diff = firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean()
var1, var2 = firsts.totalwgt_lb.var(), others.totalwgt_lb.var()
n1, n2 = len(firsts.totalwgt_lb), len(others.totalwgt_lb)

pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
d_totalwgt = diff / np.sqrt(pooled_var)
print(d_totalwgt)
```
