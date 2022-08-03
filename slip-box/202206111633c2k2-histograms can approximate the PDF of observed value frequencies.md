---
aliases: []
---
Status: #permanent-note 
Tags: [[histogram]]

>Direct quote

The histogram is *statistical* tool that graphs the observed frequencies of values occurring.[^1]

It is the statistical counterpart of the probabilistic *PDF*.[^2]

The *histogram* can be used to approximate the *PDF* of all values by dividing the frequency of occurrence of  values by the total count of outcome occurrences for all value or value buckets.[^3]

The counts of values produce by the histogram function $h(x)$ are normalized by the counts of all value $h(x)$  from the histogram function $h(x)$ [^3]

$$P(k=X)= \frac{h(k=X)}{\sum_x h(x =X)}$$

This may not be adequate for rare events, whose frequencies are approximated better through a process called *discounting*[^4]
[^1]: [[202206111633c2k1-A histogram is a statistical corollary to a PDF and from the frequency of observed events]]
[^2]:[[202206111633c2k-a probability density function represents the probability of all random variable values in a sample space]]
[^3]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 32
[^4]: