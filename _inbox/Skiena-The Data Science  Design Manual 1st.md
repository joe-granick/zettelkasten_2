---
aliases: [The Data Science Design Manual 1st, Skiena 2017, Ski+17]
---

Added: 202205091009
Name: The Data Science Design Manual
Tags: #book
Topics: [[Data Science]]
Author: [[Steven Skiena]]
Publisher: [[Springer]]
Year: [[2017]]
Edition:
URL: 
Cite:

## What kind of book is this?
A computer practical book on the topic of data science, may fall udner Computer Science, Statistics, and Math

## What is this book about?
The purpose of the book is to explain the key concepts underpinning data science. The manual attemopts to explain the underlying influences, teaching the main pricniples and getting the simple thing right over technological complications, devbelopment of mathematical intuition and howthey affect DS decisions without getting overly technical, and how to think like a compuetr scientist but act like a sattistician. This is instructed through traditional text, as well as real world projects applying the concepts many of which illustrate projects that failed and why, take home lessons with the big picture of topics, and homework problems.

## What are the major topics and how are they organized, related, and/or independent?
1. What is data science and why has it rose to prominence
2. Academic undperinnings of data science
3. Data preparation and exploration
4. Models from simple scoring and ranking heuristics to machine learning
5. Big data infrastructure to support data intensive workloads

## Chapter 1: What is Data Science?
Topic:
 [[202206121102 practical data science empahsizes getting the basics right and actionable insights]]
[[202206120752- mathematical intuition is critical for data science]]
[[202206111633 - think like a computer scientist act like a statistician understand like a domain expert]]
[[202206131033 data science is a field emerging from long established disciplines drive by changes in techology]]
[[202206131406-data science methods strongly influenced by CS methods need to be applied in a messy world like real science]]
[[202206141427-DS requires context and asking good questions of the dataset]]
[[202206141848-broad thinking is needed to find answers in unexpected data sets]]
[[202206141913-baseball has many characteristics of a good dataset for DS]]
[[202206141946-a statistical proxy is needed when specifically related measure or dataset is unobtainable]]
[[202206141944-using IMDB records to examine questions small and large scale questions related to movies]] **todo**
- **10 - 11** Google Ngrams for language data
- **11** aggregates of time series can be used to analyze historical trends
- **11 - 14** NY Taxicab data
- **12** large datasets can be used to answer questions on various scales
 [[202206151429-data can be structured or unstructured]]
 [[202206151435-data can be quantitative or qualitative]]
 **TOD:** Expand **Ordered Nominal**, **ratio scale**, **interval scale**
 [[202206151437-big data vs. small data]]
 [[202206161636-the right data is better than more data]]
 [[202206161754-supervised learning most common challenge in DS classfication or regression]]
- 17 - 18 *Quant-Shop* challenges
- 18 - Kaggle contest interviews
- 19 genius vs. wisdom in data science
### 1.7 War Stories
[[202206171234-1.7 War Story- Asking the Right Questions, solutions should be pointed and should scale|1.7 War Story- Asking the Right Questions- solutions should be pointed and should scale]]

### 1.8 References
**TODO**

### 1.9 Exercises
 **TODO:**  [[1.9 exercises]] 
## Chapter 2 : Mathematical Preliminaries
Topic:
[[202206221553p-Data Science Math Prereqs#Math Forms the Foundation of Data Science]]


### 2.1 Probability
[[202206221553p-Data Science Math Prereqs#Probability]]

#### 2.1.1 Probability vs. Statistics
[[202206241833-probability theory of future likelihood, stats applied to frequency of past events]]

**ELABORATE:**[[202206241850-probability invented by pascal and fermat assesing fair payout of unfinished game of chance]]

#### 2.1.2 Compound Events and Independence
[[202206261106-compound events use set operations to combine events and find complex probability]]

[[202206270825- independent events prob easier to calculate but  not informative for prediction and inference]]


#### 2.1.3 Conditional Probability
[[202206271239-conditional probability needed to find likelihood of an event as a function of another event]]

#### 2.1.4 Probability Distributions
[[202206271334-a probability density function represents the probability of all random variable values in a sample space]]

[[202206271758-A histogram is a statistical corollary to a PDF and from the frequency of observed events]]

[[202206271820- CDF are alternative representation of random variable prob containing same info as PDF]]

**33-34** Apple's disingenuous use of CDF over PDF because it looks better

### 2.2 Descriptive Statistics
**34** *descriptive statistics* describe and summarize important properties of datasets and samples
**34** summary statistics used for data reduction
**34** summary statistics can be used as features themselves for clusters in the dataset
**34** two main types of descriptive statistics
	- *Central tendency measures*
	- *Variation/variability measures*

#### 2.2.1 Centrality Measures
**34** *arithmetic mean* is best for describing symmetric distributions
**35** *geometric mean* more meaningful for averaging rations (see also *arithmetic mean of log of ratio*)
**35** *median* is the middle point of the dataset and is a better statistic when the distribution is skewed
**35** *mode* is most frequent item in a dataset, typically a poor measure of center for large distributions

#### 2.2.2 Variability Measures
**36** *standard deviation* and *variance* both measure on average how far observations will be from the mean
**37** population variance and sample variance have slightly different denominator

#### 2.2.3 Interpreting Variance
**37** Data scientists try to explain world through data, but often phenomena isn't really and only appears due to variance
**37** *sampling error* 
**37** *measurement error*
**37** *signal to noise ratio* degree to which observations reflect quantity of interest and not just variance
**37-38** investment performance often a matter of luck
**38-39** seasonal changes in a baseball player's performance often due to variance
**39** small differences in model accuracy typically due to variance

#### 2.2.4 Characterizing Distributions
**40** "Report both the mean and standard deviation to characterize your distribution, written as $\mu \pm \sigma$."
**39** distribnutions not necessarily concentrated towards setting, but mean and standard deviation combined do a good job of characterizing any distribution, since $\sigma$ is sensitive to points far from mean
**39** regardless of how data is distributed, for any distribution at least $(1-(1/k^2))$th of mass must lie within $\pm k$ standard deviations of means. This means at least 75% of data is within $2 \sigma$ of the mean and almost 89% within  $3 \sigma$
**39** for normal guassian distributions the bounds are even tighter

### 2.3 Correlation Analysis
**40** $x$ and $y$ are *correlated* if knowing the value of $x$ has predictive power for the value of $y$
**40** *correlation coefficient* $r(X,Y)$ measures the degree to whcih $Y$ is a *linear* function of $X$ and vice versa
**40** Empircial correlation serves as the basis for many predictive models
**40** both measures fall in range $[-1,1]$ 

#### 2.3.1 Correlation Coefficients: Pearson and Spearman Rank
##### Pearson Correlation Coefficient
**42**  *pearson correlation* defines degree to which a linear predictor can fit the data
**41** it is more prominent of two correlation measures
**41** *covariance* potentially increases with vairability of $X$ and $Y$ denominator scales it to between $[-1,1]$ 
**41** denominator of coefficient represents variance in two variables measured by *standard deviation*

##### Spearman Rank Correlation Coefficient
**42** *pearson correlation* works when function is approximatley linear, but becomes innacurate for non-linear functions and is sensitive to outliers
**42** *spearman coefficent* measures based on rank order matching of $x_i$ and $y_i$
**42** *Spearman* better suited to *non-linear monotonic* functions and is less sensitive to outliers
![[spearman_vs_pearson_skiena17_pg43.png]]

#### 2.3.2 The Power and Significance of Correlation
**43** *correlation coefficient* measured degree to which $x$ can be used to predict $y$ in a given sample $S$
**43** what's important is how well correlation holds up in real world
**43** two dimensions of assessing relevance of correlation
	- Strength of correlation
	- Statistical signifcance
**45** Weak signifcant correlation can have value in predictive modeling. Combinations of weak significant predictors **may** have predictive power depending on certain assumption holidng up (see 5.3)

#### 2.3.3 Correlation Does Not Imply Causation!
>Everyday it rains, so
>everyday the pain
>Went ignored and I'm sure
>ignorance was to blame
>But life is a chain, cause and effected.
>**Jay-Z**

**45** many observed correlations are spurious
**45** can often be hard to to determin causality, few statistical tools availabe
	- hypothesis testing
	- Instrumental Variables
**45** in cases where controlled experiments can be performed, often can only manipulate one vairable and test one direction of causality
	-can put people on a diet and observe no change in height to prove weight deosn't cause height, but can't cut off people's limbs to prove that height doesn't cause weight
	![[xkcd552_correlation.png]]
#### 2.3.4 Detecting Peridocities by Autocorrelation
**47** many human activities follow a cycle
**47** Seasonal trends result from cycles that rise and fall in a pattern
**47** *autocorrelation* used to detect cyles by correlating a sequence with itself
	- *autocorrelation function* is series of correlations for all $1\le k\le k-1$
**47** autocorrelation lets a model use previous observations as features and is useful for predictive purposes
	- for many poroblems more recent data is more predictive
	- eg today's weather is should resemble yesterday's weather
**47** autocorrelation generally strongest for for short lags
**47** long term predictions tend to be less accurate due to generally weaker autocorrelation
**47** sometimes periodicity stretches longer, and accuracy is better further out
	-preditcing weather based on data from 365 days ago more accurate than data from 180 days
**47** calculating full autocorrelation has large time complexity, but *Fast Fourier Transform* can be used to calculate autocorrelation efficiently for long sequences
![[time_series_autocorrelation17_pg46.png]]


### 2.4 Logarithms
**47** *logarithms* are the inverse of exponential function $y=b^x$
*$$b^{log_by}=y$$
**47**  exponents grow at a fast rate, and logs grow at a slow rate
**47** logarithms grow at the rate of the powers of their base $b=\{2^1, 2^2,2^3,2^4,...\}$ $log_b=\{1,2,3,4...\}$
**47** *logarithms* useful for sequences where the same number is being multiplied or divided
$$y=log_bx \longleftrightarrow b^y=x$$
**47** logarithms have 3 important roles in data science, but are useful for many more reasons in other domains (*see algorithm design manual*)

#### 2.4.1 Logarithms and Multiplying Probabilities
**48** logarithms historically used to simplify computation by turning multiplication to addition
**48** still useful today to multiply long hcains of probabilities, as they can yield very small numbers, which lose stability with floating point representation on computers and can cause numerical errors
**48** can raise to exponent if real probability needed, but usually fine to compare proability by size of log
**48** be aware of that logs of proabilities are negative except $log(1)=0$, and are often prepened w/ a negative sign

#### 2.4.2 Logarithms and Ratios
**48** *ratios* can occur as natural features or ones derived from feature pairs
**48** occur naturally in normalizing data for conditions or time, representing the change in relation to an intital state of the world
	- conditions: weight after treatment over intital weight
	- time: today's price divided by yesterday's price
**48** complication of ratios is that increases and decreases are not symmetric in magnitude for the same absolute change
	- 200/100 is an increase of 200%
	- 100/200 is a decrease of 50%
**48** this means averaging ratios can be misleading
**48** geomertic mean could be used, but better approach is to take the log of the ratios which result in equal displacement for changes of same absolute magnitude
	- $log_22=1$ and $log_2(\frac{1}{2})=-1)$
**48**  bonus is that sign follows the direction of the change
**48** visualization of ratio changes is much more straightforward to interpret when log scaled
![[plotting_ratios_skiena17_pg49.png]]
#### 2.4.3 Logarithms and Normalizing Skewed Distributions
**50** normal distributions are nice to work with due to their symmetry, but many processes create non-guassian distribution where there is a high skewness to the data
**51** logarithms can be used to transform power law distributions into a guassian form known as the *log normal distribution*
**51** if *logarithm* is to extrem of a transformation other functions can be used like taking the square root, test is which results in a more symmetric distribution

### 2.5 War Story: Fitting Designer Genes
**52** developing scoring functions that highlight a certain aspect of the data can reveal patterns
**52** often these type of scores are ratio calulations, and benefit from being tranformed logarithmically

### 2.6 References
[[Henk Tijms. Understanding Probability. Cambridge University Press, 2012.]]
[[Understanding-Probability (Henks 3rd.  2012).pdf]]

[[Dimitri Bertsekas and John Tsitsklis. Introduction to Probability. Athena Scientific, 2nd edition, 2008.]]
[[Introduction to Probability (bertsekas, 2nd, 2008).pdf]]

[[Gareth James, Daniela Witten, Trevor Hastie, and Robert Tibshirani. An Introduction to Statistical Learning. Springer-Verlag, sixth edition, 2013]]

[[Charles Wheelan. Naked Statistics: Stripping the dread from the data. WW Norton & Company, 2013.]]

[[Warren Weaver. Lady Luck. Dover Publications, 1982.]]

### 2.7 Exercises

## Scoring and Ranking
[[202206071016-Optimizing Search Engines using Clickthrough Data|learning rannking functions]]
[[202206071022-A FAST & EFFECTIVE HEURISTIC FOR THE FEEDBACK ARC SET PROBLEM|minimize edge conflicts]]
## Statistical Analysis
[[50 Years of data science]]
[[James, Witten, Hastie, Tibshirani- Introduction to Statistical Learning 2nd]]
[[How to Lie With Statistics]]
[[Naked Statistics]]

## Visualization
## Mathematical Models
## Linear Algebra
**dot product** measures correlation in the same way as the **Pearson correlation**
$cos(\theta)$  is the same as the correlation of two mean zero variables (pg 241)
- both range from \[-1,1]
- identical vectors are perfectly correlated
-  antipodal points are perfectly negatively correlated
- orthogonal vectors have no correlation
**matrix multiplication** (pg 243)
- not commutative
- associative 
**covariance matrix** (245)
- magnitude captures degree to which row or column pairs move together
- **adjaceny matrix** used to represent vertices and edges for graphs
- **permutation matrix**

**matrix rank** (pg 251)
- number of linearly independent rows
- feature matrices may be of lower rank than desirable
	- duplicate entries
	- duplicate columns
	- increase rank so all rows linearly independent by adding noise
- **condition number** in a linear system how sensitive $X$  is to small changes in $Y$ in $Y = AX$
**factoring matrices** (pg 252)
- many ML algorithms can be represented in terms of factoring a matrix
- factoring yeilds more concise matrix representation
- example would be converting sparse matrix of 50,000 words in tweets down to 100 most frequent topics, with each row as a tweet, can be compared along the similiarity of topics
	- useful for many probnlems involving language as features [[word embeddings]]

**Eigenvalues and Eigenvectors**
- **Single value decomposition(SVD)** is a more genral matrix facotization apporach than eigenvalyue **decompositions**(pg 260)
- SVD can be used to reduce dimensionality of matrices
- **Principal Compnent Analysis** does same thing as SVD but from a different direction
- PCA/SVD serve equally well as low-dimenisonal approximations of a featrue matrix
- **Dimensionality reduction** create new dimensions as **linear combinations** of the originals, higly correlated dimensions are collapsed into a lower dimensional space
- Reduced dataset is tupically cleaner, not just a reduction of dimensions.  Relatively few features explain bulk of variance, and relatively few compnents capture the sturcture of the point set. Residula is mostly noise, and when removed typically results in cleaner dataset
### Linear/Logistic Regression
linear regression serves as a good baseline, can then be approached with more adavnce ML techniques of additional value is worth additional effort (pg 267)

**linear regression** finds line of best fit through givens set of lines (268)
- main use is for forecasting but has many aopplications
	- compressing and simplifying data, replacing noisy set of points on x y plane witha line
	- usefelu for visualizing relationship between points and shows:
		- trend
		- outlier location and magnitude
**relationship with linear equations** (268)
- *linear eaquations* searching for single point that lies on $n$ lines
- regression given $n$ points and want to find line that lies through "all" points
	- in this case it's the line of best approximation for all points
**least squares regression with matrices** (271)
- least squares define x=(A^_TA)^_-1A_^Tb so regression reduces to inverting and multiplying matrices
- works well for small matrices
- **gradient descent** more efficient for large datasets     
**fitting non-linear functions**
- " if you want a functioon to be linear, measure it at only two points"
- **support vector machines** can include non-linear terms without being explicitly enumerated
### logistic regression
**hierarchial classiication**   for multi-class label preditcion
- combines [[binary trees]] with logistic regression where each node is a classifier distinguishing left and right descendants (299) 





[^8]:[[The Data Science  Design Manual]] pg 4
[^9]:https://www.baseball-reference.com/
[^10]:[[The Data Science  Design Manual]] pg 6