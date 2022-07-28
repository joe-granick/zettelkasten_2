---
aliases: [Robustness]
---
202206131945
Status: #idea
Tags: [[CS vs Science]]
Links:

Scientists account for the fact that datasets have errors.[^1]

To contain the impact on their work they consider the data generating process and how bias,  and noise can be introduced, how it can affect their results, what may be indicative of error, what can be done to mitigate the impact or how the study/interperetation should be adjusted and what can be done to prevent it going forward.

Computer scientists on the other hand assume data doesn't have errors. Their concern is how the data is processed, and are the operation/calculation done correctly. Errors they may be concerned with formatting and type errors and use data validationa and typing systems to prevent this. 

However since the actual results aren't relevant to their objectives, the correctness of the data input in the algorithm doesn't matter.  [^2]

To them it's "garbage in garbage out" the state of the data sits in an abstract box that are the concerns of others. [^1]

[^1]:[[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual]] pg 3
[^2]:[[202206111633e-scientists focus on results and answers unlike CS]]

