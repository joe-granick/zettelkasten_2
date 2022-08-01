---
aliases: []
---
Status: #permanent-note 
Tags: [[probability distribution]], [[probability density function]], [[random variable]], [[probability]]

Random variables are functions that take *outcomes* in a *sample space* and returns a numerical value for the event defined by the function.[^1]

For a *random variable* $V(s) =X$ the probability of the value $X$ is the sum of the probabilities of all outcomes in the sample space that produce $X$ when input into the *random variable* function $V(s)$[^2]

For the entire *sample space* the probabilities of the random variables can be mapped onto a *probability density function(PDF)* that represents the  the probabilities of all *random variables* produced by the outcomes contained in the *sample space*.[^2]

This *PDF* takes the form of a graph where the $x-axis$ represents all possible *random variable* values produced by the sample space and the $y-axis$ denotes the probability of that value occurring.[^2]

![[pdf_cdf-data_science_design(lecture_2-slide_5).png]]

The statistical representation of a $PDF$ is a *Histogram*, which represents the frequency of random variable values based on the actual observed frequency of outcomes[^3] 

*PDF*s are probabilistic and represent the likelihood that the next observation will have the value of that particular *random variable*.[^2]

A *PDF* can be approximated from the histogram.[^4]

A *cumulative density function (CDF)* is an alternative representation of the probabilities of random variables, it contains the same info as a *PDF* and either can be converted from the other.[^5]


[^1]: [[202206111633c2f-Random Variable  a FUNCTION that takes outcomes as input]]
[^2]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 32
[^3]:[[202206111633c2k1-A histogram is a statistical corollary to a PDF and from the frequency of observed events]]
[^4]:[[202206111633c2k2-histograms can approximate the PDF of observed value frequencies]]
[^5]:[[202206111633c2k3- CDF are alternative representation of random variable prob containing same info as PDF]]