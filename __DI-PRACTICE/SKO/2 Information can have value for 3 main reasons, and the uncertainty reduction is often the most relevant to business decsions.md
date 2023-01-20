Information can have three kinds of value:

1.  Information can affect people’s behavior (e.g. common knowledge of germs affects sanitation behavior).
2.  Information can have its own market value (e.g. you can sell a book with useful information).
3.  Information can reduce uncertainty about important decisions. (This is what we’re focusing on here.)

When you’re uncertain about a decision, this means there’s a chance you’ll make a non-optimal choice. The cost of a “wrong” decision is the difference between the wrong choice and the choice you would have made with perfect information. But it’s too costly to acquire perfect information, so instead we’d like to know which decision-relevant variables are the _most_ valuable to measure more precisely, so we can decide which measurements to make.

Here’s a simple example:

> Suppose you could make $40 million profit if [an advertisement] works and lose $5 million (the cost of the campaign) if it fails. Then suppose your calibrated experts say they would put a 40% chance of failure on the campaign.

The expected opportunity loss (EOL) for a choice is the probability of the choice being “wrong” times the cost of it being wrong. So for example the EOL if the campaign is approved is $5M × 40% = $2M, and the EOL if the campaign is rejected is $40M × 60% = $24M.

The difference between EOL before and after a measurement is called the “expected value of information” (EVI).

In most cases, we want to compute the VoI for a range of values rather than a binary succeed/fail. So let’s tweak the advertising campaign example and say that a calibrated marketing expert’s 90% CI for sales resulting from the campaign was from 100,000 units to 1 million units. The risk is that we don’t sell enough units from this campaign to break even.

Suppose we profit by $25 per unit sold, so we’d have to sell at least 200,000 units from the campaign to break even (on a $5M campaign). To begin, let’s calculate the expected value of _perfect_ information (EVPI), which will provide an upper bound on how much we should spend to reduce our uncertainty about how many units will be sold as a result of the campaign. Here’s how we compute it:

1.  Slice the distribution of our variable into thousands of small segments.
2.  Compute the EOL for each segment. EOL = segment midpoint times segment probability.
3.  Sum the products from step 2 for all segments.

Of course, we’ll do this with a computer. For the details, see Hubbard’s book and the Value of Information spreadsheet from [his website](http://www.hubbardresearch.com/htma-downloads/).

In this case, the EVPI turns out to be about $337,000. This means that we shouldn’t spend more than $337,000 to reduce our uncertainty about how many units will be sold as a result of the campaign.

And in fact, we should probably spend much less than $337,000, because no measurement we make will give us _perfect_ information. For more details on how to measure the value of _imperfect_ information, see Hubbard’s book and these three LessWrong posts: (1) [VoI: 8 Examples](https://www.lesswrong.com/lw/cih/value_of_information_8_examples/), (2) [VoI: Four Examples](https://www.lesswrong.com/lw/85x/value_of_information_four_examples/), and (3) [5-second level case study: VoI](https://www.lesswrong.com/lw/8j4/5second_level_case_study_value_of_information/).

I do, however, want to quote Hubbard’s comments about the “measurement inversion”:

> By 1999, I had completed the… Applied Information Economics analysis on about 20 major [IT] investments… Each of these business cases had 40 to 80 variables, such as initial development costs, adoption rate, productivity improvement, revenue growth, and so on. For each of these business cases, I ran a macro in Excel that computed the information value for each variable… [and] I began to see this pattern: * The vast majority of variables had an information value of zero… * The variables that had high information values were routinely those that the client had never measured… * The variables that clients [spent] the most time measuring were usually those with a very low (even zero) information value… …since then, I’ve applied this same test to another 40 projects, and… [I’ve] noticed the same phenomena arise in projects relating to research and development, military logistics, the environment, venture capital, and facilities expansion.

Hubbard calls this the “Measurement Inversion”:

> In a business case, the economic value of measuring a variable is usually inversely proportional to how much measurement attention it usually gets.

Here is one example:

> A stark illustration of the Measurement Inversion for IT projects can be seen in a large UK-based insurance client of mine that was an avid user of a software complexity measurement method called “function points.” This method was popular in the 1980s and 1990s as a basis of estimating the effort for large software development efforts. This organization had done a very good job of tracking initial estimates, function point estimates, and actual effort expended for over 300 IT projects. The estimation required three or four full-time persons as “certified” function point counters…

> But a very interesting pattern arose when I compared the function point estimates to the initial estimates provided by project managers… The costly, time-intensive function point counting did change the initial estimate but, on average, it was no closer to the actual project effort than the initial effort… Not only was this the single largest measurement effort in the IT organization, it literally added _no_ value since it didn’t reduce uncertainty at all. Certainly, more emphasis on measuring the benefits of the proposed projects – or almost anything else – would have been better money spent.

Hence the importance of calculating EVI.^[ https://www.lesswrong.com/posts/ybYBCK9D7MZCcdArB/how-to-measure-anything]