

>[!info]
More than 50 years ago, John Tukey called for a reformation of academic statistics. In ‘The Future of Data Analysis’, he pointed to the existence of an as-yet unrecognized science, whose subject of interest was learning from data, or ‘data analysis’. Ten to twenty years ago, John Chambers, Bill Cleveland and Leo Breiman independently once again urged academic statistics to expand its boundaries beyond the classical domain of theoretical statistics; Chambers called for more emphasis on data preparation and presentation rather than statistical modeling; and Breiman called for emphasis on prediction rather than inference. Cleveland even suggested the catchy name “Data Science” for his envisioned field." ^[ [[50 Years of data science]]]

- Why not use nueral nets?
	- ANN for tabular data research
- Where does data centric ML and Quality come into play?
- **Idea:** automation of repetitive decisions can be accomplished by combining even simplest analytics rooted in descriptive statistics with predicate logic
	- use of data and statistical analysis to find causality and model Truthiness/ Falseness of propositions based on conditional variables
	- simple statistics can be used to evaluate the to state of conditions and execute decision/task/simulation based on value and proposition
	- can continue to monitor to see if assumed relationships hold
- Data Science Paradigm of **Data analysis Meta Research**
	- consultancies should use sample of companies to study generalizable problems and research
- [[2 don't bikeshed casaulity]]
- **Bikeshedding** causality ^[  [[https://thecodersblog.com/analaysis-Parkinson's-law-of-triviality/]] ]
	- executives may make decisions based on gut intuition these scenarios don't need data 
	- misunderstanding leading to comments and attitudes like this from business stakeholders and 
- **Descriptive Stats**
	- Useful for developing shared understanding of business abstractions and ability to translate  ideas and progress across those abstractions
	- May be useful for adding nuance to to high-touch human dependent processes where summaries different entities can add helpful context to decision making (eg operational analytics help salespeople better understand customer needs and behavior )
	- [[5 descriptive stats are useful to monitor data allowing rapid ability for operational decisions to adapt to the situation on the ground]]
		- best of this is seamless (yelp, google)
		- can be composed for heuristics rankings to create simple models and structured "best practice" decision making
- [[3 vanity metrics are to be avoided]]
- [[4 best types of metrics are "twitchy" facilitating rapid ability to respond]]
	- cumulative sales
- **Causal inference**
- [[1 metrics must be aligned with strategic incentives]]
- **Capital One** case study show that more sophisticated unlocks ability to measure more valuable metrics and and ask more valuable questions [[]]
- Is something measurable
	- can an observable construct be defined
	- how reliably does this construct represent the unobserved variable
- Evaluate if level of rigor and sophistication of methods are appropriate for 
	- maturity of analytic solution 
	- value of problem
	- sophistication of audience
	- elements that are crucial for audience to understand (relevant to stakeholder problem)
- communication needs to combination of simplified clear translations of results and improved data literacy of audience
	- easier to teach someone with an 8th grade reading level than 4th grade
	- difficult to understand calculus if you never learned algebra
- **descriptive stats** and understanding of data and data generating process facilitates identification of anomalies and errors ^[[[Foster, Fawcett-Data Science for Business]]]
- measures of accuracy
- expected value, calibration, and decision thresholds
- Bayesian Reasoning
- Foxes vs. Hedgehogs
- Cognitive biases
- Noise in decision making
- Monte Hall Problem
- How much accuracy is needed where decision is valuable?
	- what does this mean for decision making?
	- what does this mean for AI based features?
- Domain knowledge important for effective feature engineering
	- feature stores
- for monitoring want to define assumptions and relationship, as well as measure of validity

> [!info]
 The trouble with your brain
In the previous century, it was fashionable to praise anyone who stuffed a fat wad of math into some unsuspecting human endeavor. Taking a quantitative approach is usually better than thoughtless chaos, but there’s a way to do even better.
>
Strategies based on pure mathematical rationality are relatively naïve and tend to underperform.
>
Strategies based on pure mathematical rationality without a qualitative understanding of decision-making and human behavior can be pretty naïve and tend to underperform relative to those based on joint mastery of the quantitative and qualitative sides. (Stay tuned for blog posts on the history of rationality in the social sciences as well as examples from behavioral game theory where psychology beats mathematics.)
>
Humans are not optimizers, we’re satisficers, which is a fancy word for corner cutters.
>
Humans are not optimizers, we’re satisficers, which is a fancy word for corner cutters who are satisfied with good enough as opposed to perfect. (It’s also a concept that was enough of a shocker to our species arrogance—a punch in the face of rational Man, godlike and flawless — that it was worth a Nobel Prize.) ^[ https://towardsdatascience.com/introduction-to-decision-intelligence-5d147ddab767]

>[!info]
>“He uses statistics as a drunken man uses lamp-posts… for support rather than illumination.” -Andrew Lang ^[https://towardsdatascience.com/introduction-to-decision-intelligence-5d147ddab767]

>[!info]
 If you care about an "intangible" it is because it has observable consequences and usually you care because knowing more would inform a decision. Everything else is a matter of rigorously defining what you observe, why you care about it, and some mostly trivial math. ^[ [[How to Measure Anything]] pg 7]

>[!info]
>**Why measure in the first place**
>- Informs a key decision
>- Has monetary value on it's own
>- Entertains or satisfies a curiosity
>The following points support the need for measurement
> 1. Decisions are made under imperfect information
> 2. Decisions should be made via quantitative models, as the models have a favorable track record compared to expert judgement
> 3. Measurements inform uncertain decisions
> 4. For any decision/decisions there is a large combination of elements to measure and ways to measure them, perfect certainty is rarely an option ^[ [[How to Measure Anything]] pg 7]
- Management needs analyze options for reducing uncertainty^[ [[How to Measure Anything]] pg 7]

- Expert intuition is needed, but has limits. All ranks of decision makers need to know when expert judgement is called for vs when to use a quantitative model instead^[ [[How to Measure Anything]] pg 7]
- measurements are multi-step chains of thought, inferences can be made from indirect observations^[ [[How to Measure Anything]] pg 18]

- [[Fermi Decomposition]] helps estimate an uncertain quantity, but the explicit structuring also helps identify where the uncertainty came from^[ [[How to Measure Anything]] pg 18]
	- biggest source of uncertainty should point to a measurement that would reduce uncertainty
	- helps us evaluate our current state of knowledge as a precursor to further measurement^[ [[How to Measure Anything]] pg 25]
technically not a measurement since it includes no new observation^[ [[How to Measure Anything]] pg 18]
	- is really an assessment of what info we know already


- Intangible goals **must** still have observable consequences if they truly matter^[ [[How to Measure Anything]] pg 22]
	- employee empowerment
	- creativity
	- strategic alignment
- tools of scientific inquiry useful for observing variety of phenomena^[ [[How to Measure Anything]] pg 22]
	- controlled experiments
	- sampling
	- randomization
	- blinding
- Revenue is an important measure, but before evaluating whether something had an impact on that metric you need to figure out if it had an impact at all. That depends on measuring an observable outcome that changed after implementation^[ [[How to Measure Anything]] pg 24]
- Measurement is **uncertainty reduction** not uncertainty *elimination*^[ [[How to Measure Anything]] pg 25]
	- avoid defeatist attitudes, small reductions may be worth a lot even if it is in formal structure finding where uncertainty lies
	- value depends on frequency of decision and magnitude of uncertainty
>[!info]
>**Misconceptions About Impossibility of Measurement**
>Often times people will claim something can't be measured because of lack of knowledge around the following concepts^[ [[How to Measure Anything]] pg 29]
>1. *Concept of measurement.* Definition of measurement of ten misunderstood.
>2. *Object of measurement.* Thing being measured is not well defined.
>3. *Methods of measurement.* Procedures of empirical observation are not well known. When people become familiar many more things will seem measurable.

- [[Shannon entropy]] and measurement scales related to the definition of measurement ^[ [[How to Measure Anything]] pg 30 - 34]
- Bayes theorem ^[ [[How to Measure Anything]] pg 34]
- **Methods of measurement**
	- rule of 5^[ [[How to Measure Anything]] pg 42] 
	- Urn of mystery^[ [[How to Measure Anything]] pg 44]

> "If you don't know what to measure, measure anyway. You'll learn what to measure 
> - David Moore^[ [[How to Measure Anything]] pg 48]

> "It is impossible to find any domain in which humans clearly outperform crude extrapolation algorithms, less still sophisticated statistical ones"
> - Phillip Tetlock^[ [[How to Measure Anything]] pg 52]

>[!info]
>**Four Useful Measurement Assumptions**
>1. It's been measured before.
>2. You have more data than you think.
>3. You need less data than you think.
>4. Usefule new observations are more accessible than you think
> Shouldn't dismiss something as unmeasurable outright^[ [[How to Measure Anything]] pg 59]



