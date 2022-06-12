---
aliases: [The Data Science Design Manual, Skiena 2017, Ski+17]
---

Added: 202205091009
Name: [[The Data Science Design Manual]]
Tags: #book
Topics: 
Author: [[Steven Skiena]]
Year: [[2017]]
Edition:
URL: 
Cite:

## What kind of book is this?
A computer practical book on the topic of data science, may fall udner COmputer Science, Statistics, and Math

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
vi do the simple things right more important than latest tech

vi importance of mathematical intuition

[[202206111633 - think like a computer scientist act like a statistician understand like a domain expert]]

1 influences on DS

1 why DS gaining popularity now

2 DS on the spectrum between Computer Science and Real Science

2 - 3 Computer Scientist vs Natural/Social Scientist treat data differently 

3 Data scientists need to turn nimbers into insights and shoudl think like *"real scientists"* in support of this

4 DS requires context and context is built by curiosity and asking good questions of data sets... another way DS and CS are differentiated

5 Broad thinking - answers to big general questions can often be hidden in specific datasets outside of original intended purpose 

5 Baseball records make great datasets for data science

7 Data scientists need to be pragmatic, **statistical proxy** may be needed, as dataset explicitly for desired purpose likely doesn't exist

9 IMDB as direct data and statistical proxy

10 - 11 Google Ngrams for language data

11 aggregates of time series can be used to analyze historical trends

11 - 14 NY Taxicab data

12 large datasets can be used to answer questions oon various scales

14 - 16 Data properties 
	- structred v. unstructured
	- Quantitative vs. Categorical
	- Big Data vs. Small Data

16 *take home lesson* - the right data is better than more data

16 supervised learning tasks typicallly either **classification** and **regression**

17 - 18 *Quant-Shop* challenges

18 - Kaggle contest interviews

19 genius vs. wisdom in data science

20 answering right question and solving problems with business value more important than ability to do anything.. "world will notbeat a path to your door for just a new source of data. You must be able to supply the right questions before you can turn data into money."

22 - 23 - more info on sources (baseball, google ngram, ny taxi)
### contents
### data science, computer science, real science
- data science lies at the intersection of computer science, statistics, and applied domains  (pg 1) 
- DS more popular due to recent advancements
> think like a computer scientist acta like a statisticican (pg vi)

> *computer scientists* produce *systems* **data scientisits** produce **insights** (pg 3)
#### computer science vs real science
data scientists aim to turn numbers into insights and therefore are foucsed on the **why** of a problem/solution like *real scientists* as well as the **how** like *computer scientists* (pg 2)

data scientists should adopt a scientific mindset, and not just limit themselves to the viewpoint of computer science (pg 3)

the following points of view are important differences that data scientists need to adapt from science vs the traditional CS philosophy

**data centrism vs. method centrism**
	1
**emphasis on results**

**robustness**

**precision vs. accuracy**

#### data driven vs hypothesis driven science (pg 3)
*hypothesis forward:* given a **problem** what data will help solve or answer it

*data forward:* given a dataset what problems or opportunities can it be applied to

#### domain expertise and questions [^8]
- important for data scientists to be curious about the world and the context of the data they work with
- have to aske questions of domain experts
##### baseball encyclopedia [^9]

**five questions** [^10]
1. how has player salary changed over time?
2. what stats are most related to winning?
3. are there players in the market that are undervalued and is there a specific aspect of their game that is systemically undervalued or missed?
4. are certain positions overrepresented by lefties compared to the general population?
5.  what are the thematic elements undelrying player description metadata?

#### latent questions
- often interesting questions, patterns, and problems are hidden within data sets with entirely different purposes
- baseball's 150 years of detailed record keeping contains demographic info on populations that can act a as [[statistical proxy]] for populations note extensively studied
	- baseball data can study life-span of righties vs lefties, one of few sources that contains extensive data on handedness?
	- can study likelihood of people returning to where they were born after travelling?
	- do salaries reflect past,present, or future performance?
	- How have height and weight changed over time?

- data scientists need to be pragamatic, and use the data available because the perfect dataset is often unaccessible if it even exists
### properties of data
#### structured vs. unstructured
#### quantitative vs. categorical 
#### big data vs. small data
- big data isn't always necessary and can often overcomplicate things, and goal should not be to blindly analyze massive datasets. For example it is likely more effective to poll a representative sample of the greater population about voter preferences, ratehr than trying to amplify latebnt sentiments across massive unstructured data sets from socail media feed


### classification vs. regression
### Probability
- **experiment**
- **sample space**
- **event**
- **probability of outcome**
- **probabilty of event**
- **random variable**
- **expected value**

## Scoring and Ranking
[[202206071016-Optimizing Search Engines using Clickthrough Data|learning rannking functions]]
[[202206071022-A FAST & EFFECTIVE HEURISTIC FOR THE FEEDBACK ARC SET PROBLEM|minimize edge conflicts]]
## Statistical Analysis
[[50 Years of data science]]
[[Introduction to Statistical Learning]]
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





[^8]:[[Data Science  Design Manual]] pg 4
[^9]:https://www.baseball-reference.com/
[^10]:[[Data Science  Design Manual]] pg 6