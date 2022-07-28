---
aliases: []
---
Status: #idea
Tags: [[conditional probability]], [[bayes theorem]], [[classification]]

The *conditional probability* defines the likelihood of the of one event as a function of another event.[^1]

This becomes useful for predictive purposes when there is a dependence or a correlation between events, with certainty of the event in question increasing as the dependence with the variable it is being conditioned on increases.[^2]

For two events *A* and *B* the conditional probability of *A* give *B* is[^1]
$$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$$

This is particularly useful in *classification*  where the task can often be reduced to finding the conditional *probability* of an observation belonging to class where we know a *correlated* variable is true or false.[^4]

The dependency however makes the calculations more difficult, while independent probabilities are trivially straightforward. [^3]

*Bayes theorem* is commonly used to compute conditional probabilities. It reverse the direction of the dependence, which often makes the task easier since it may be easier to observe events in the opposite directions[^5]

[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 31
[^2]: [[202206111633c2h2-correlations are critical to predictive modeling and inference]]
[^3]: [[202206111633c2h1- independent events prob easier to calculate but  not informative for prediction and inference]]
[^4]:[[202206271315-classification can often be reduced to finding conditional probability]]
[^5]: [[202206111633c2h14-bayes theorem simplifies conditional probability by reversing the dependence]]