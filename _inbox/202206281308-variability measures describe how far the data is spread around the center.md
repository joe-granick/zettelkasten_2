---
aliases: []
---
Status: #idea
Tags: [[standard deviation]], [[variance]], [[variability measures]]

Variance measures characterize how the spread of observations around the center of the distribution. That is the average distance from the mean observations fall above or below.[^1]

The two main measures of variance are *standard deviation* and *variance*, they produce different numbers but contain the same information.[^1]

Variability adds important information to summarizing the distribution as it measures the amount of uncertainty about the *mean* where higher variance means less certainty of how far observations will likely fall around the mean.[^2]

The sum of squares penalty makes variance highly susceptible to outliers[^3]

Population and sample variance/sd have different denominators (n vs n-1 respectively), but as sample increases the sample variance/sd should approach the population variance/sd[^4]


#### Standard Deviation
*Standard deviation* is the most common measure of variability which is the sum of squared distances between the observations and mean.[^1]

This contains the same info as the *Variance* but usually makes more sense as taking the root it normalizes the variability to the same unit of measure as the observation.[^1]

##### Sample Standard Deviation

$$\sigma= \sqrt{\frac{\sum^n _{i=1}(a_i-\bar a)^2}{n-1}}$$

##### Population Standard Deviation
$$\sigma= \sqrt{\frac{\sum^n _{i=1}(a_i-\bar a)^2}{n}}$$
#### Variance
*Variance* is the squared standard deviation $V= \sigma^2$, it contains the exact same information as the *standard deviation* but may be easier to talk about because it is shorter.[^1]

##### Sample Variance

$$V= \frac{\sum^n _{i=1}(a_i-\bar a)^2}{n-1}$$

##### Population Variance
$$V= \frac{\sum^n _{i=1}(a_i-\bar a)^2}{n}$$




[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 36
[^2]:[[202206281655-mean and standard deviation combined do a good job characterizing any distribution]]
[^3]:[[202206281640-sum of squares penalty makes variance sensitive to outliers, one point d units adds as much variance as d^2 points one unit]]
[^4]:[[202206281646-sample deviation approaches population as the sample size approaches infinity]]