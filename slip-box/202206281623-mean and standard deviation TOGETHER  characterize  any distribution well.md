---
aliases: []
---
Status: #idea
Tags: 

The mean does a good job of characterizing the average observation, but it leaves a lot of information about the distribution unclear.[^1]

This is because the probability mass doesn't necessarily need to be concentrated around the mean.[^2]

Together the mean and standard deviation together do a good job of describing any distribution $\mu \pm \sigma$.[^3]

Adding a measure of variability characterizes the distance to expect observations to fall from the mean[^1]

Due to the standard deviations sensitivity to outliers a small amount of variance greatly increases the deviations, so a small $\sigma$ means the observations are strongly concentrated around the mean.[^4]

For any distribution at least 75% of the observations must be within $2 \sigma$ of the mean and 89% within $3 \sigma$ of the mean.[^5]

For a normal distribution the bounds are even tighter allowing more certainty wrt where observations are expected to fall.[^6]
 





[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 37
[^2]: [[202206281707-mass of probability not necessarily concentrated close to the mean]]
[^3]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 39
[^4]: [[202206281640-sum of squares penalty makes variance sensitive to outliers, one point d units adds as much variance as d^2 points one unit]]
[^5]:[[202206281948-For all distributions75% of data must be within 2 SD of mean and 89% within 3 SD]]
[^6]:[[202206281955-for a normal distribution 68% of data in one SD of mean 95% in two and 99.7 within 3]]

