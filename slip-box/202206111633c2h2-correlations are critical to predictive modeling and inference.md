---
aliases: []
---
Status: #idea
Tags: [[correlation]], [[perfect correlation]]

For predictive models to work the occurrence of one event needs to have some dependence on another event that can either be more easily observed, or leads the occurrence of the event of interest.[^1] 

This dependence is known as a *correlation*. When event *A* is correlated with event *B* that means that knowing that an event occurred reduces the uncertainty of the likelihood of its correlated event occurring.[^1] 

At the extreme are events that are perfectly correlated, where know that one event occurred is perfectly prediction of its correlate occurring. For example if I **always** bring an umbrella (*event A*) if it is raining (*event B*) and it rains $(B=1/5)$ of the time then  the likelihood of carrying an umbrella is $(A= 1/5)$, and is just their joint probability[^3]  and knowing that it is raining $(B=1)$ means that it can be predicted that I will bring an umbrella $(A=1)$.[^1]

Perfectly correlated events are the opposite of independent events where knowing that one event occurred tells nothing about another event occurring.[^2] 

The dependency between correlated events makes calculating their joint probability much more difficult, as the conditional probability calculations can be complicated.[^3]

[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 31
[^2]: [[202206111633c2h1- independent events prob easier to calculate but  not informative for prediction and inference]]
[^3]: [[202206111633c2h-compound events use set operations to combine events and find complex probability#set intersection]]