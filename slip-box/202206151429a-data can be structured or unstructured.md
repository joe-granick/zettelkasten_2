---
aliases: []
---
Status: #permanent-note 
Tags: [[data properties]], [[structured data]], [[unstructured data]]
Links: [[202206151429a1-unstructured data typically can be pre-processed into a structure for analysis|202206151429a1]]

**Structured data** 
Structured data has an explicitly defined structure or schema. Data is normalized in a form ready for querying, analysis. [^1]

Readily adaptable as input for learning algorithms, each observation us represented as a **feature vector**, ith one output and unlimited input. 

Conceptually represented as a **matrix** where each observation is a row, and each feature is a column within that row. Easily represented/stored in spreadhseets and relational databases. 

**Unstructured data** 
Unstructured data may have an implicit structure, but it is not standardized or defined. These sources contain info, but it is in a heterogenous structure. Examples include text, images, and website/pages/links.[^1]

Something like text data has an implicit structure, but it is based on context and not in a state ready for querying, analysis, and learning.[^2]

There are methods to convert the implcit structure of this type of data into a format suitable for analysis and machine learning. For example **bag of words** can be used to turn text into a matrix.[^1][^2]



[^1]:[[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual]] pg 14
[^2]:[[Foster, Fawcett-Data Science for Business]] pg 252
