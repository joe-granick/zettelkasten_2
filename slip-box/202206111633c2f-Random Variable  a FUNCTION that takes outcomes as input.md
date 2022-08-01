---
aliases: ['202206111633c2f']
---
Status: #permanent-note 
Tags: [[probability]], [[random variable]]

#### Random Variable
A $\text{random variable, denoted V}$ is a function that maps *outcomes* in a *sample space* to a numerical value. [^1]

The frequency of random variable values from the outcomes in the sample space represents the probability distribution for the values produce by the variable[^1]

For a craps game, the random variable would be the function that sums the value of the two dice for each outcomes. $V(a,b)=a+b$ which has random variables of integer values in the range $[2,12]$. 

The probability distribution is composed of the sum probability of all outcomes of dice roles that  produce the same random variable value. This is done for each possible random variable value possible with the sample space as input. For the *random variable* $V(s) = X$, s made up of all *outcomes* in the *sample space* that produce the to the value $X$ when input *random variable* function $V(s)$ [^1]

For the rolls where the random variable $V(s)= 7$:[^1]
$$
\begin{align} 
p(V(s)=7)=1/6 \hspace{20cm}\\
\text{because:} \hspace{21.8cm}\\ 
S_{\in V(s)=7}=\{(1,6),(6,1),(2,5),(5,7),(3,4),(4,3)\} \hspace{13.3cm}
\end{align}$$

Meanwhile for the rolls where the random variable $V(s)= 12$:[^1]
$$
\begin{align} 
p(V(s)=12)=1/36 \hspace{20cm}\\
\text{because:} \hspace{21.8cm}\\ 
S_{\in V(s)=12}=\{(6,6)\}\hspace{19.5cm}
\end{align}$$

The probability of all random variables can be represented by a *Probability Density Function (PDF)*[^2] or a *Cumulative Density Function (CDF)*[^3]

[^1]: [[Skiena-The Data Science  Design Manual 1st|The Data Science Design Manual 1st]] pg 28
[^2]: [[202206111633c2k-a probability density function represents the probability of all random variable values in a sample space]]]
[^3]:[[202206111633c2k3- CDF are alternative representation of random variable prob containing same info as PDF]]