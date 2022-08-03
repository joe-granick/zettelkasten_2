---
aliases: []
---
Status: #permanent-note 
Tags: [[cumulative density function]]

*CDF*s are an alternative to *PDF*s for representing the probability of *random variables*. While different in form from the *PDF* both contain the same exact information.[^1]

The *CDF* represents a running sum of the total probability in the *PDF*, where the *CDF* monotonically increases with the random variable values.[^1]

The *CDF* can be computed by the *PDF* and represents the probability of the outcome being less than or equal to the current value.[^1]
$$C(X \le k) = \sum_{x \le k}P(X=x)$$
CDF continue to increase as values rise until it contains the probability of all random variables with the highest value equal to 1. $C(X \le \infty)=1$, care must be taken as this can be used deceptively as a vanity metric.[^2]

Since they both contain the same info they can be easily converted into the other form

$$P(k=X) = C'(k) = C(X \leq k ) - C(X \leq k - \delta)$$
where $\delta=1$ for integer distributions[^1]
[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 33
[^2]:[[202206271838-care must be used with CDFs so it is not abused as avanity metric]]