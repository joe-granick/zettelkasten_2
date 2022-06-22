---
aliases: [data vs. algorithms]
---
Status: #idea
Tags: 

>
**Mind Versus Data**
>
Progress in the last decade shows that the success of an ML system depends largely on the data it was trained on. Instead of focusing on improving ML algorithms, most companies focus on managing and improving their data.[16](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/ch02.html#custom_ch02fn1)
>
Despite the success of models using massive amounts of data, many are skeptical of the emphasis on data as the way forward. In the last five years, at every academic conference I attended, there were always some public debates on the power of mind versus data. _Mind_ might be disguised as inductive biases or intelligent architectural designs. _Data_ might be grouped together with computation since more data tends to require more computation.
>
In theory, you can both pursue architectural designs and leverage large data and computation, but spending time on one often takes time away from another.[17](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/ch02.html#ch01fn50)
>
In the mind-over-data camp, there’s Dr. Judea Pearl, a Turing Award winner best known for his work on causal inference and Bayesian networks. The introduction to his book _The Book of Why_ is entitled “Mind over Data,” in which he emphasizes: “Data is profoundly dumb.” In one of his more controversial posts on Twitter in 2020, he expressed his strong opinion against ML approaches that rely heavily on data and warned that data-centric ML people might be out of a job in three to five years: “ML will not be the same in 3–5 years, and ML folks who continue to follow the current data-centric paradigm will find themselves outdated, if not jobless. Take note.”[18](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/ch02.html#ch01fn51)
>
There’s also a milder opinion from Professor Christopher Manning, director of the Stanford Artificial Intelligence Laboratory, who argued that huge computation and a massive amount of data with a simple learning algorithm create incredibly bad learners. The structure allows us to design systems that can learn more from less data.[19](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/ch02.html#ch01fn52)
>
Many people in ML today are in the data-over-mind camp. Professor Richard Sutton, a professor of computing science at the University of Alberta and a distinguished research scientist at DeepMind, wrote a great blog post in which he claimed that researchers who chose to pursue intelligent designs over methods that leverage computation will eventually learn a bitter lesson: “The biggest lesson that can be read from 70 years of AI research is that general methods that leverage computation are ultimately the most effective, and by a large margin.… Seeking an improvement that makes a difference in the shorter term, researchers seek to leverage their human knowledge of the domain, but the only thing that matters in the long run is the leveraging of computation.”[20](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/ch02.html#ch01fn53)
>
When asked how Google Search was doing so well, Peter Norvig, Google’s director of search quality, emphasized the importance of having a large amount of data over intelligent algorithms in their success: “We don’t have better algorithms. We just have more data.”[21](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/ch02.html#ch01fn54)
>
Dr. Monica Rogati, former VP of data at Jawbone, argued that data lies at the foundation of data science, as shown in [Figure 2-7](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/ch02.html#the_data_science_hierarchy_of_needsmoni). If you want to use data science, a discipline of which ML is a part of, to improve your products or processes, you need to start with building out your data, both in terms of quality and quantity. Without data, there’s no data science.
>
The debate isn’t about whether finite data is necessary, but whether it’s sufficient. The term _finite_ here is important, because if we had infinite data, it might be possible for us to look up the answer. Having a lot of data is different from having infinite data.[^1]
> ![[data_hierarchy_of_needs.png]]
 Figure 2-7. The data science hierarchy of needs. Source: Adapted from an image by Monica Rogati[22](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/ch02.html#ch01fn55)[^2]

[^1]:[[Huyen-Designing Machine Learning Systems]] ch 3
[^2]:[[The AI Hierarchy of Need]]