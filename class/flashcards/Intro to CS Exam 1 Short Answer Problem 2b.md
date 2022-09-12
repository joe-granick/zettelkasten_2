#flashcards/intro-to-cs/exam-1 
(25 points) Tax Rate. The amount of tax paid by a family will be determined based on several factors, including gross income earned by family (A), dividend income from investments (B), savings interest earned(C), home mortgage interest(D), number of dependents supported (E), and amount of charitable donations(F). In a hypothetical situation, we assume the following. 
1. gross income, dividend, and savings interest are taxable 
2. the family is allowed to deduct $6000 per dependent from total income 
3. home mortgage interest is tax-deductible up to $10,000 (that is, any interest paid over $10,000 cannot be deducted) 
4.  charitable donations up to 10% of gross income are tax-deductible. 
5. dividend income from investments (B) is taxable at a fixed rate of 8% 
6. adjusted income is computed by subtracting deductions (D, E) from gross income + savings interest (A+C) 
*NOTES: The total taxes on adjusted income (`adjusted income * tax Rate`) are computed according to the following rules.* 
1. The first $50,000 of the adjusted income is computed at a tax rate of 8% 
2. The next $100,000 of the adjusted income is computed at a tax rate of 20% Excess adjusted income over $150,000 is computed at a tax rate of 33% 
	a. **Example 1** if a family has an adjusted income of $175,000, then their tax is calculated as = `50,000*0.08 + 100,000*0.20 + (175,000-150,000)*0.33 + dividend tax`
	b. **Example 2** a family with adjusted income of $82,000 will pay = `50000*0.08 + (82000-50000)*0.20 in taxes + dividend tax`. 
	c. **Example 3** a family with adjusted income of `$42,000 will pay = 42,000*0.08 in taxes + dividend tax`
The taxes for dividends must be calculated separately and added to the tax total. Write a program in pseudocode to compute the total taxes for a family.
?
``` md
READ grossIncome
READ dividendIncome
READ savingsInterest
READ mortageInterest
READ numDependents
READ charitableDonations
SET totalTaxes to 0
COMPUTE totalIncome AS grossIncome + savingsInterest
IF mortageInterest > 10,000
SET mortgageInterest TO 10,000
ENDIF
IF charitableDonations > .10*grossIncome
SET charitableDonations TO 0.10*grossIncome
ENDIF
COMPUTE deductibleAmount AS numDependents*6000 +
charitableDonations + mortageInterest
COMPUTE taxableIncome AS totalIncome - deductibleAmount
IF taxableIncome > 150000
COMPUTE totalTaxes as totalTaxes +(taxableIncome -
150,000)*0.33
SET taxableIncome AS taxableIncome – 150,000
ENDIF
IF taxableIncome > 50000
COMPUTE totalTaxes as totalTaxes + (taxableIncome -
50,000)*0.20
SET taxableIncome AS taxableIncome – 50,000
ENDIF
COMPUTE totalTaxes as totalTaxes + (taxableIncome)*0.08
COMPUTE totalTaxes AS totalTaxes + dividendIncome*0.08
DISPLAY totalTaxes
```