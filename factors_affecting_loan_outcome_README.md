# Analysis of the Factors Contributing to Loan Status Outcome.
## by Freda Victor


## Dataset

>  The Loan data by Prosper contains 113,937 observations with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. 

> For this analysis I worked on 14 variables from the data namely Term, LoanStatus, BorrowerAPR, BorrowerRate, ListingCategory, BorrowerState, EmploymentStatus, IsBorrowerHomeowner, CreditScore, DebtToIncomeRatio, IncomeRange, LoanOriginalAmount, Recommendations and Investors. 

> I was most interested to answer 'what factors affect a loan’s outcome status in the dataset?'


## Summary of Findings

> Univariate Analysis

For Univariate Analysis, I explored the following questions:
1. What is the count of the variable of interest LoanStatus?
2. What is the distribution of numeric variables BorrowerRate, BorrowerAPR and DebtToIncome?
3. What are the counts of qualitiative variables BorrowerState, EmploymentStatus, IncomeRange and IsBorrowerHomeowner?

Findings:
1. My variable of interest the LoanStatus has its highest distribution in the current status followed by completed status counts then the chargeoff. LoanStatus had different past due observations such as (past due 1-15 days, past due 31-60 days etc) which I had to group into an overall past due for cleaner plotting.

2. Of the features investigated see below the operations done:

   -DebtToIncomeRatio: The data is overly skewed to the right, so I used a log scale and set the x-limits to show points of interest.This made the data have a normal distribution for exploration.
    
   -ListingCategory: I swapped the listing category values with its meaning to better understand what the values represented e.g 1 for debt consolidation. 
    
   -EmploymentStatus: I tidied the EmploymentStatus variable by grouping all employment status (full-time, part-time, self-employed etc) to employed for cleaner plotting.

> Bivariate Analysis

To start off Bivariate analysis, I explored the following questions:
1. What numerical variables are correlated with one another? The variables were Term, BorrowerAPR, LoanOriginalAmount, BorrowerRate, DebtToIncomeRatio, Investors, Recommendations and CreditScore.
2. What is the relationship between LoanStatus and two numeric variables BorrowerRate and CreditScore?
3. What is the relationship between LoanStatus and two qualitative variables EmploymentStatus and IncomeRange?

Findings:
1. There is an expected relationship between LoanStatus and BorrowerRate as the plot shows that Borrowers who did not complete their loan payments had a higher interest rates and lower creditscores when compared to those Borrowers who completed their loan payments. Also more of the loans where given to those who are employed. 
2. BorrowerRate, BorrowerAPR, CreditScore, Investors, Term and LoanOriginalAmount had interesting negative or positive relationships with one another. 
    - BorrowerRate and BorrowerAPR have very strong positive correlation.
    - Both BorrowerRate and BorrowerAPR have strong negative correlation with CreditScore.
    - Both BorrowerRate and BorrowerAPR have a negative correlation with Investors.
    - Investors and CreditScore have weak positive correlation.
    - Term and CreditScore have weak positive correlation.
    - DebtToIncomeRatio and BorrowerRate have very weak positive correlation.
    - Investors, CreditScore and Term have positive correlation with LoanOriginalAmount
    - Both BorrowerRate and BorrowerAPR have a negative correlation with LoanOriginalAmount.
    
> Multivariate Analysis

For multivariate analysis, I explored the following questions:
1. What is the relationship between LoanStatus, BorrowerRate and IsBorrowerHomeowner?
2. What is the relationship between LoanStatus, Investors and IsBorrowerHomeowner?
3. What is the relationship of LoanStatus against BorrowerRate and CreditScore?
4. What is relationship between EmploymentStatus against LoanStatus and BorrowerRate?

Findings:

1. I extended my investigation of LoanStatus in this section by looking at the impact of BorrowerRate against several variables in the dataset. The multivariate exploration showed that Borrowers with completed status had a lower borrower's rate compared to past due, defaulted or chargedoff status.
2. When IsBorrowerHomeOwner is added, we can see that most borrowers who own a home had lesser borrower rates compared to those that do not own homes. I also noticed a lower borrower rates for those who completed and own homes. Borrowers with completed loan payments also had more investors compared to those who defaulted, past due or charged off.In addition, as Borrower's CreditScore increases, borrower's interest rates decreases.
3. From investigation, it was interesting to see that you are most likely to get and complete payment of a loan when you employed. Interest rates also seems lower when employed. Looking back on the scatter plot, it was surprising to see that there was no clear relationship between Borrower's CreditScore and LoanStatus.

Conclusion

Based on my analysis, the factors that affect a loan's outcome are BorrowerRate, EmploymentStatus, IsBorrowerHomeowner, and Investors. 



## Key Insights for Presentation

> My key insights:

1. To show the factors that affected a loan’s outcome status, I explored several features to support this argument. Although there were a lot of variables in the dataset, After going through the data dictionary, I selected certain variables that I instinctively thought would be good factors that can influence loan status outcome such as EmploymentRate and BorrowerRate.Others were selected due to how they would respond or influence other variables chosen e.g ListingCategory and IsBorrowerHomeowner.

2. For the explanatory report, I want to show how the chosen variables influenced my analysis from the univariate to multivariate and also give recommendations on how to potentially look out for certain factors while giving out loans inorder to avoid loan default.


















