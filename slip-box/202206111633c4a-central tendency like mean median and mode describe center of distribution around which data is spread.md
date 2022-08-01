---
aliases: ['202206111633c4a']
---
Status: #permanent-note/elaborate  
Tags: [[arithmetic mean]], [[geometric mean]], [[harmonic mean]] [[median]], [[mode]], [[f-mean]]
# Average
https://en.wikipedia.org/wiki/Average

## Mean
https://en.wikipedia.org/wiki/Mean

### Pythagorean Mean
https://en.wikipedia.org/wiki/Pythagorean_means

#### Arithmetic Mean
*Arithmetic mean* is describes the absolute balance point of a distribution.[^1]

It is sensitive to outliers, and is most useful for symmetric distributions[^2]

It is calculated by the sum of all observation divided by the total number of observations.[^1]
$$ \mu_x = \frac{1}{n} \sum_{i=1}^nx_i $$
The mean can easily be updated with the addition of new data or removal of data by keeping the count and sum separate, then dividing at the time of need.[^1]

Arithmetic mean is also doesn't adequately capture the central tendency when averaging ratios. The *geometric mean* or the average of the *log* should be used instead[^3][^4]

#### Geometric Mean
Geometric mean is calculated by taking the nth root of the product of the observations in a data set. [^5]

$$(\prod^n _{i=1}a_i)^{1/n} = \sqrt[n]{a_1a_2...a_n}$$ 
The *geometric mean* will always be smaller than the *arithmetic mean* and it very sensitive to zero values, which will completely 0 out the result. (This is analogous to an observation value of $\infty$ in an arithmetic mean)[^5]

The *geometric mean* more meaningful for averaging ratios, as the *arithmetic mean* of ratios doesn't show the true property of the distribution [^3]

#### Harmonic Mean
[[202206111633c4a1c-harmonic mean measures average rate]]

### Generalized Mean
https://en.wikipedia.org/wiki/Mean#Generalized_means

#### Generalized f-mean
## Median
The median measure the exact center value of a distribution, this is the point where 50% of values lie above the value and 50% lie below.[^5]

The *arithmetic mean* is useful for symmetric distributions but is extremely sensitive to outliers[^2]

In these cases the median is often a better way to characterize the center of the distribution.[^6]

Additionally the median value is an actual value of an observation, which is not true of the mean.[^5]

## Mode
The *mode* is most frequent item in a dataset, typically a poor measure of center for large distributions. This is usually a matter of coincidence, but may be useful for identifying errors and anomalies[^7]

A more useful way to characterize the most frequent observations is by the peak in a frequency distribution or histogram as long is the values ranges are bucketed in a meaningful way.[^8]

[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 34
[^2]: [[202206111633c4a1a-arithmetic mean most useful for symmetric distributions but is sensitive to outliers]]
[^3]:[[202206111633c4a1b-geometric mean captures central tendency of ratios better than arithmetic mean]]
[^4]:[[202206111633c4a1b1-ratios should be log transformed before taking their arithmetic mean]]
[^5]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 35
[^6]:[[202206111633c4a2-median is a better measure than mean for datasets with outliers and skewed distributions]]
[^7]:[[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 36
[^8]:[[202206271807-histogram value ranges may be bucketed for representative clarity]]