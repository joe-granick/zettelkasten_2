---
aliases: []
---
Status: #idea
Tags: [[probability]]

#### Probability of an Event
The $\text{probability of event E, denoted } p(E)$ is the sum of all individual probabilities of the outcomes. [^1]
$$p(E) = \sum_{s \in E}p(s)$$

It can be alternatively formulated  in terms of the *complement of the event* $\bar {E}$. This is useful for many situations where $p(\bar E)$ is easier to calculate than $p(E)$[^2]
$$P(E)=1-p(\bar E)$$

For a craps game the probability of winning is the sum of all proabilities of the winning event space 
$$E = \{(1,6),(2,5),(3,4),(4,3),(5,2),(6,1),(5,6),(6,5)\}$$
These outcomes have the probabilty 
$$\begin{aligned}  
p(1,6) = (1/36)\\
p(2,5) = (1/36)\\
p(3,4) = (1/36)\\
p(4,3) = (1/36)\\
p(5,2) = (1/36)\\
p(6,1) = (1/36)\\
p(5,6) = (1/36)\\
p(6,5) = (1/36)\end{aligned}$$

Therefore the sum of the probabilty of an Event equaling a winning role:
$$p(E=win) = (8/36)$$


[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 28
[^2]: [[202206111633c2j-complement prob useful alternative that often simplifies prob calculation]]