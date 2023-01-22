#interactive
Taking a random sample of 5 from a population of any size there is a 93.75% chance that the population median is between the highest and lowest value of in the sample. ^[[[How to Measure Anything]] **pg 43-44**]

# Math of why this works
Since by definition the 50% of all values lie above the median, and the other 50% lie below it. Therefore the probability that a randomly selected value lies above the median is 50% (likewise for below). Therefore  the probability of randomly selecting 5 values above the median is 1/32. Using the same logic for the probability of 5 values below, we sum the probabilities t 6.25% chance of randomly selecting a value above or below the range of the 5 values or a 93.75% probability that the median is within that range^[[[binomial distribution]]], [[independent probability]]

$$
P(x>median) = (\frac{1}{2})
$$

$$
P(x>median*5) = (\frac{1}{2})^5 = (\frac{1}{32})
$$
