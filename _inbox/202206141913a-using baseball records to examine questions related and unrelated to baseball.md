---
aliases: [baseball records related and unrelated questions]
---
Status: #permanent-note/elaborate 
Tags: [[statistical proxy]]

Due to the the extensive records kept and the length of time they have been kept for, many trends can be examined and questions asked both directly related to baseball and not related at all.

**Directly related questions**: The most straightforward questions are the ones directly related to baseball[^1]
	- *How should a player's skill/value be measured?* [^1]
	- *Generally,how fair are trades?*[^1]
	- *How does player performance change as they get older?*[^1]
	- *Is batting correlated with a player's position?*[^1]

**Unrelated questions:** With 150 years of data on 20,000+ players, interesting questions can be asked examined by that apply to the general population. The dataset contains extensive tracking of human and societal characteristics that are not extensively tracked elsewhere. [^7]

With a broad view, some context knowledge, and imagination the study of baseball can be used to study the general population. [^3]

In this capacity the population of the baseball dataset is used as a **statistical proxy**[^4], where there is a lot of data recorded for baseball players that hasn't been recorded, analysis of the baseball data can generalize to the population of interest (human beings, society).
	- *Do left-handed people have different lifespans than right-handed people?* Most demographic datasets don't capture handedness, and don't have the volume nor time horizon of data captured in the baseball datatset.[^2] 
		- This is a question that has actually been studied using baseball records (left-handedness)[^5] 
	- *Do people return to the places they were born?* Baseball players birth and death locations extensively documented means this question can be studied in their population and could be indicative of behavior for the general population. Interestingly the structure of the game means players are typically exposed to more locations than the general population. This can conceivably be used to ask conditional questions about if people are more likely to move away after seeing variety of locations[^2]
	- *Are salaries correlated with past, present, or future performance?* Salary and performance data extensively tracked, can be analyzed at the population levels and salaries and how they vary with performance of players at various points in their career. [^2]
	- *How have heights and weights changed in the population over time?*

Data scientists should be careful about drawing causal conclusions, and should take care when trying to generalize to the population at large.  Statisticians know that the dataset contains **sampling bias** (only male, more athletic population, higher salaries etc.).[^6],[^7]  This doesn't mean it can't be used to study the world, the data-generating process just needs to be taken into account when determining the confidence in the results.[^8]
![[leftorium.jpg]]

[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual]] **pg 6**
[^2]:[[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual]] **pg 7**
[^3]:[[202206121102b-broad thinking is needed to find answers in unexpected data sets]]
[^4]:[[202206111633e4a1-a statistical proxy is needed when specifically related measure or dataset is unobtainable|202206111633e5a]]
[^5]:[[Do right-handers live longer]]
[^6]:[[202206111633b - think like a computer scientist act like a statistician understand like a domain expert]]
[^7]:[[202206111633a-data science methods strongly influenced by CS methods need to be applied in a messy world like real science]]
[^8]:[[202206150826-bias in sample population needs to be accounted for when generalizing results]]

