# Prosper Loans Data Exploration
## by Pedro Cruz


## Dataset

The dataset consist of informations of about 113,937 loan listings with 81 features.  
Feature docummentation available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0)


## Summary of Findings

In the exploration, I found that the variable of interest, "BorrowerAPR", have a high, or almost perfect, correlation with variables that seem to be affected by it, namelly "BorrowerRate", "LenderYield", "EstimatedLoss", "EstimatedEffectiveYield" and "EstimatedReturn", but it was not possible to find those kind of strong correlations with variables that, possiblly, have an affect on it.

Both the ProsperScore and the StatedMonthlyIncome, that innitially I though to be the most relevant for setting the BorrowerAPR, proved to have very low correlation with it (-0.27 and -0.17 for the ProsperScore and the StatedMonthlyIncome, respectivelly).

Worth mentioning that the 'StatedMonthlyIncome' variable has a distribution extremmely skewed to the right, requiring to limit the data in order to get meaningfull information. For the most part, to avoid overplotting, the limit was set at the 75% percentile (7k USD), while on others it was possible to limit at 99.9% (44k USD). The full range goes up to 1,750k USD.

Going forward, I looked for correlations between the BorrowerAPR and StatedMonthlyIncome adding to the mix all combinations of the following boolean variables 'IncomeVerifiable', 'CurrentlyInGroup' and 'IsBorrowerHomeowner'. unfortunately, none of those attempts generated a higher correlation with the "BorrowerAPR".


Other interesting findings:
* regarding the "BorrowerAPR", it was found that the mode of the distribution is exactly 35,797%. Such rate represents 3.22% of all loans, strongly suggesting that this rate is some type of standard rate.
* In addition, it was possible to understand a little of the profile of the Prosper user. More than 50% them listed the purpose of the loans as debt consolidation and more than 50% (not necessarily the same 50%) of them stated incomes in the range between 25k and 75k USD.


## Key Insights for Presentation

For the presentation, I focus on the influence of the income in the borrowerAPR, leaving out the analysis of variables that added little to the understanding of the variable of interest.
I start by introducing the BorrowerAPR variable, followed by the distribution of the StatedMonthlyIncome and its characteristics regarding outliers to the right.
Finally, I look at the relationship between BorrowerAPR and income, where I focus both for the income in USD thousands and for the boolean variable that states whether a stated income is verifiable or not.