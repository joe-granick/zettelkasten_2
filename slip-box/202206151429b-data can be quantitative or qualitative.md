---
aliases: ['202206151429b']
---
Status: #permanent-note 
Tags: [[data properties]],[[quantitative data]], [[qualitative data]], [[dsicrete scale]], [[continuous scale]], [[nominal variable]], [[ordinal variable]]

## Quantitative data
**Quantitative data** are variables measured by numerical values. [^1] 
These variables are either measured on a **discrete scale** or **continuous scale** [^2]

Quantitative variables are natuarally used in formulas, and mathematical models and are well suited to visualizations in many standard and exotic visualizations.[^1]

### Discrete scale
### Continuous scale

## Qualitative data
**Qualitative data** or *categorical data* are variables that represent the class label for data like hair color, gender, occupation etc. [^1]

This type of data is meaningful, but required different techniques to work with. [^1]

### Nominal data
Most commonly in the form of **nominal data**.[^4] This type of data can be coded as numerical data where the label is a binary variable indicating whether it is a member of the class label or not. For example *gender* coded as a variable where $gender = 0$ means male and $gender = 1$ means female[^1]

However the numeric encoding is meaningless beyond the binary true and false values.

With more than two character per feature, things get more complicated. For hair color coding each color as a separate number doesn't make sense, as no hair color is numerically larger than another (max and min color don't make sense)[^1]

With multiple categories separate variables will typically be needed for $n-1$ of the categorical labels, where each variable is 0 if it the obsevation doesn't fit that label, and is 1 if it does ($n-1$ where all zeros is the default category). 

Most methods are built for **quantitative data** there are methods built specifically to work with categorical data[^1] **Clustering** and **Classification** create labels from **quantitive inputs**[^3]

### Ordinal data
**Ordinal data** is categorical data with a ranked ordering between classes, but the size of difference between classes is meaningless (example, small, medium, and large shirts)[^5]

[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual]] pg 15
[^2]: [[Statistics 4th Edition. Freedman, Pisani, Purves]] pg 43
[^3]:[[202206161407-Classification and Clustering algorithms generate categorical labels as output from data]]
[^4]:[[202206161412-nominal data is categorical data where variable represents class membership of the label]]
[^5]:[[202206161414-ordinal data is catgorical data where labels represent rank differnces but the size of the difference is meaningless]]
