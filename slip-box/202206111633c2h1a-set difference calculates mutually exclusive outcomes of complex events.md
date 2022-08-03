---
aliases: ['202206111633c2h1a']
---
Status: #permanent-note 
Tags: [[set difference operation]]

A compound event is made up of the  combined outcomes of the individual events in the composition[^1]

These combined events must have at least one differentiating outcome, otherwise they would be considered the same event.[^2] 

For example if event ***A*** is a dice roll where at least one of the two dice are even[^2]
$$\begin{align}
A= 
\{(1,2),(1,4),(1,6),(2,1),(2,2),(2,3), (2,4),(2,4),(2,5),(2,6),\\
(3,2),(3,4),(3,6),(4,1),(4,2),(4,3),(4,4),(4,5),(4,6),(5,2),\hspace{-0.3cm}
\\ 
(5,4),(5,6),(6,1),(6,2),(6,3),(6,4),(6,5),(6,6)\} \hspace{2.1cm}
\end{align}$$

With and event ***B*** for all outcomes where the sum of the dice roll add up to **7** or **11**  [^2]
$$B=\{(1,6),(2,5),(3,4),(4,3),(5,2),(5,6),(6,1)(6,5) \}$$

Then the set difference operation for the outcomes of ***A*** that are not outcomes of ***B***
$$\begin{align}
A-B= 
\{(1,2),(1,4),(2,1),(2,2),(2,3), (2,4),(2,4),\\
(2,6),(3,2),(3,6),(4,1),(4,2),(4,4),(4,5),\hspace{-0.09cm}
\\ 
(4,6),(5,4)(5,4),(6,2),(6,3),(6,4),(6,6)\} \hspace{0.0cm}
\end{align}$$

Note that one event can encompass the entirety of another event, as long as it has more outcomes that are not in the smaller event space. The set difference operation for all outcomes of **A** not in **B** produces an empty set, as only an even number can be added to an odd to make another odd (7 or 11). Therefore the set difference is empty as the outcome space of **A** contains the entire outcome space of **B** (A is a [[superset]] of B)[^2]
$$B-A=\{\}$$


[^1]: [[202206261106-compound events constructed from composiition of outcomes in the sample space]]
[^2]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 30