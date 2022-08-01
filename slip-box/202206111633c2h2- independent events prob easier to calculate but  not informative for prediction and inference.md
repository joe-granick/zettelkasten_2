---
aliases: ['202206111633c2h2']
---
Status: #permanent-note 
Tags: [[independent probability]], [[correlation]]

The probability of the intersection of *independent events* is equal to the total combined probability of both events occurring. Two events *A* and *B* are independent if and only if[^1]
$$P(A \cap B) = P(A) \times P(B)$$
When events are independent there is no common structure between their probabilities meaning knowing whether one event occurred gives no additional information about the likelihood of the other event(s). [^1]

This means the *conditional* probability of event *A* given *event B* is just the probability of *event A*.[^4]
$$P(A\mid B)=\frac{P(A\cap B)}{P(B)} =\frac{P(A)P(B)}{P(B)}=P(A)$$

This property of independence makes calculating compound probabilities much simpler computationally, but it is useless for predictive and inferential purposes. [^2]

When trying to predict one event from another it is the correlation that is important, as it reduces the uncertainty about the event being conditioned.[^3]


[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 30
[^2]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 31
[^3]: [[202206111633c2h2a-correlations are critical to predictive modeling and inference]]
[^4]: [[202206111633c2h3-conditional probability needed to find likelihood of an event as a function of another event]]