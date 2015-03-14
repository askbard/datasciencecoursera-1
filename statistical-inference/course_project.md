
<!-- https://class.coursera.org/statinference-012/human_grading/view/courses/973520/assessments/4/submissions -->
<!-- https://rstudio-pubs-static.s3.amazonaws.com/26693_e1151035722942b2813c0063c6b220ae.html -->
# The Exponential Distribution -- An Investigation with R
#### Author: Danilo Mutti


According to the [Wikipedia](http://en.wikipedia.org/wiki/Central_limit_theorem], the central limit theorem (CLT)), the central limit theorem (CLT) states that, given certain conditions, the arithmetic mean of a sufficiently large number of iterates of independent random variables, each with a well-defined expected value and well-defined variance, will be approximately normally distributed, regardless of the underlying distribution. That is, suppose that a sample is obtained containing a large number of observations, each observation being randomly generated in a way that does not depend on the values of the other observations, and that the arithmetic average of the observed values is computed. If this procedure is performed many times, the central limit theorem says that the computed values of the average will be distributed according to the normal distribution (commonly known as a "bell curve").

This report aims at investigating the exponential distribution in R and comparing it with the Central Limit Theorem. The exponential distribution can be simulated in R with `rexp(n, lambda)` where `lambda` is the rate parameter. The mean of exponential distribution is `1/lambda` and the standard deviation is also `1/lambda`. The investigation consists of one thousand simulations, each one them comprised of the averages of 40 exponentials. The value of lambda used in the `rexp` function is fixed in 0.2 for all of the simulations.

The specific objectives of this report are the following:

1. Show the sample mean and compare it to the theoretical mean of the distribution.
1. Show how variable the sample is (via variance) and compare it to the theoretical variance of the distribution.
1. Show that the distribution is approximately normal.

## Simulation

In order to keep this report reproducible, we must set a random seed -- a number on which the random number stream depends on -- so the reader can obtain exactly the same numbers in his/her R environment when following the steps presented in this report. In our case, the seed is set to the integer number `12345`.


```r
set.seed(12345)
```