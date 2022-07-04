---
aliases: []
---
Status: #idea
Tags: [[geometric mean]], [[ratios]]

For averaging ratio values, the *arithmetic mean* does a poor job of characterizing the distribution. There is "less room" for ratios to be below 1 than above which creates an asymmetry that the *arithmetic mean* overstates.[^1]

For example the *arithmetic mean* of $2/1$ and $1/2$ is $1.25$[^1]

The *geometric mean* on the other hand creates a more meaningful average where the result of $2/1$ and $1/2$ results in 1.

This makes sense when taken from the point of view of doubling vs halving something, as if I double something then take half of it the result should be the baseline value.

Alternatively the arithmetic mean of the *log* of the ratios can be used[^2]

[^1]:[[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 35
[^2]: [[202206281230-ratios should be log transformed before taking their arithmetic mean]]