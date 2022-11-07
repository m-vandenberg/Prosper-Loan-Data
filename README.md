# Prosper Loan Data Exploration
## by Monique van den Berg


## Dataset

The Prosper loan dataset contains 113,937 loans with 81 variables on each loan.
The dataset contains information about the borrower, the loan and some risk metrics.
The following features were explored: ProsperScore, CreditScoreRangeLower,
CreditScoreRangeUpper, IncomeRange, Term, LoanOriginalAmount, Investors, BorrowerRate
and BorrowerAPR. 
The dataset can be downloaded with this [link](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1581581520570000),
with the data dictionary available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).


## Summary of Findings

In the bivariate exploration, I found that there was a strong correlation between BorrowerAPR and BorrowerRate.
This is expected though as BorrowerAPR is BorrowerRate plus fees. I also found that BorrowerAPR had
a negative relationship with all of the remaining variables (LoanOriginalAmount, Investors, CreditScoreRange,
IncomeRange and ProsperScore) except Term. Interestingly there is no correlation between BorrowerAPR and Term.

I discovered that ProsperScore, Investors, LoanOriginalAmount, CreditScoreRange and IncomeRange are positively correlated with one another.

I also discovered that a 36 months loan term is prefered.

I extended my investigation of which variables effect BorrowerAPR, by creating multivariable plots of Term, ProsperScore, Investors, LoanOriginalAmount and BorrowerAPR. The multivirate exploration revealed the following:

Term has a slight effect on the relationship between BorrowerAPR and Investors and no effect on the relationship between BorrowerAPR and LoanOriginalAmount.

ProsperScore has a surprising effect on the relationship of BorrowerAPR with both LoanOriginalAmount and Investors. An increase in ProsperScore changes the correlation between BorrowerAPR and both LoanOriginalAmount and Investors. In both cases the correlation changes from either positive to negative or vice versa. 

The relationship between Term, ProsperScore and BorrowerAPR changes at a ProsperScore of 3 and 6. For a prosper score between 1 and 3 a lower term results in a lower BorrowerAPR. For a prosper score between 3 and 6, a higher term results in lower BorrowerAPR. At a prosper score of 7 or higher, a higher term results in a higher BorrowerAPR.

The relationship between Term, ProsperScore and Investors changes at a ProsperScore of 4, 8 and 10. For a prosper score between 1 and 5 a lower term results in a higher number of investors. For a prosper score between 4 and 8, term has no effect. At a prosper score of 8, 9 and 11, a 36 month term results in a higher number of investors. At a prosper score of 10, a higher term results in a higher number of invetors. 

There is a positive relationship between Term, ProsperScore and LoanOriginalAmount.

## Key Insights for Presentation

For the presentation, I wanted to look at the features which would significanlty affect BorrowerAPR. The main focus was on the LoanOriginalAmount, ProsperScore and Term.

I started of by showing the distrubtion of BorrowerAPR and LoanOriginalAmount. Next I showed the relationship between BorrowerAPR and both LoanOriginalAmount and ProsperScore. I didn't show a distribution plot of ProsperScore as it can be seen from the relationship graph that ProsperScore can take on a value of 1 to 11. I also didn't show the relationship between Term and BorrowerAPR as there is no correlation.

Then I showed the effect ProsperScore has on the relationship between BorrowerAPR and LoanOriginalAmount. I also showed the effect Term has on the relationship between BorrowerAPR and LoanOriginalAmount. I didn't show a distribution plot of Term as it can be seen from the relationship graph that Term can only take on three values, 12, 36 and 60 months.

Lastly I showed the effect that ProsperScore and Term both have on BorrowerAPR. 