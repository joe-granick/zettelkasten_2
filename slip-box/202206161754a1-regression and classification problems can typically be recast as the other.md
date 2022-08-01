---
aliases: ['202206161754a1']
---
Status: #permanent-note 
Tags: [[classification]], [[supervised learning]], [[regression]]

**Classification** and **Regression** are the two main tasks of *supervised learning, with supervised learning being the main type of predictive task within data science.*^[[[202206161754a-supervised learning most common challenge in DS classification or regression|202206161754a]]]

Despite on the surface solving different problem types with completely separate type of output, problems of one type can often be recast as another.

Not all problems can be reframed this way, and if the output is an input to something else a numeric or categorical output may be necessary. However where one output can be substituted for another, a creative data scientist can recast the problem if the output of the initial approach doesn't reach the desired level of accuracy or consistency.

Identification of where reframing will be beneficial as well as appropriate problem casting and recasting depend heavily on understanding the context of the problem and the structure of the data and analysis.^[[[202206121102a-DS requires context and asking good questions of the dataset|202206121102a]]]^[[[202206111633a2- data vs method centrism CS vs Science for DS|202206111633d]]]

## recasting classification and regression^[[[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual]] pg 17]

| problem framing     |question 1   | question 2  |
| -------------- | ----------------------------------------------------- | --------------------------------------------------- |
| classification | *Will the price of a stock go up tomorrow?*   | *Is selling life insurance to this person a risk?*    |
| regression     | *What will the price of a stock be tomorrow?* | *How many more years will is this person live?* |               |                                                       |                                                     |
