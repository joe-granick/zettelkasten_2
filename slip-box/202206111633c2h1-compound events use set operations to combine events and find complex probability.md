---
aliases: ['202206111633c2h']
---
Status: #permanent-note 
Tags: [[probability]], [[compound event]], [[set difference]], [[set intersection]], [[set union]], [[set complement]]

![[setdiff_intersect_union_skiena17_pg30.png]]
*Figure: Venn diagrams illustrate for events A and B the set difference((left), set intersection(middle), and set union (right)*

#### compound event
Questions of interest usually involve the composition of multiple individual events from the same sample space. These complex event compositions are termed *compound events* and are made up of the combined outcomes of the induvial underlying events. [^1]

Compound events have their own set of vocabulary for operating on them. Allowing for complex event probabilities to be composed from the outcomes of the underlying simpler events spaces.

The probability for any set can be calculated by summing probabilities of outcomes in defined sets[^1]

#### set difference
Each event in can share outcomes, but must have at least one differentiating outcome, otherwise it should be considered the same event. The *set difference operation* is defined by the outcomes that exist in one event but not another.[^2]

#### set intersection
The *intersection* of two or more sets is made up of all sets they have in common. For two sets *A* and *B* the intersection is denoted $A \cap B$ [^1]
$$A \cap B = A - (S-B)$$
The formulation shows that the intersection can be thought of as taking removing the complement of one set from the other. Many times the complement is easier to work with than the direct event.[^3]

#### set union
The *union* of two or more set is made up of all outcomes from included sets joined together. For two sets *A* and *B* their union is denoted[^1] $$A \cup B$$
#### set complement
Set complement operation calculates the inverse probability of an event, or the probability of all outcomes in a set not related to the event.

For an event *A* it's *complement set* is denoted [^1]
$$ \bar A = S-A$$
Now the probability of *A* can be calculated from the complement
$P(A) = 1 - P( \bar A)$ which is useful in many cases where calulating the probability of A is compuationally intensive[^3]

[^1]:[[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 30
[^2]:[[202206111633c2h1a-set difference calculates mutually exclusive outcomes of complex events]]
[^3]: [[202206111633c2c1-complement prob useful alternative that often simplifies prob calculation]]