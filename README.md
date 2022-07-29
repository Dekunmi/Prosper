# Exploratory Analysis of Loan Data from Prosper

## by Rachael Olakunmi Ogunye



## Dataset

> There are 113,937 entries in the main dataset with 81 features. The subset dataset (df_loan) consists of 83982 loan entries with 21 features (including LoanOriginalAmount, BorrowerAPR, StatedMonthlyIncome, ProsperRating (Alpha), EmploymentStatus and many others). Most variables are numeric in nature. The main dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv),
with feature documentation available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0). 


> The dataset was loaded onto a dataframe and assessed for quality and tidiness issues. The subset dataset was made and cleaned to limit the amount of features being assessed. The exploratory analyses (Univariate, Bivariate and Multivariate) was done to figure out the features that are best for predicting the Borrower's Annual Percentage Rate (APR) which is the main variable of interest and how Loan original amount and Prosper ratings associate with various metrics in the dataset.

> The cleaned dataset was saved as 'CleanedLoanData.csv' and consists of 83736 entries and 21 features.



## Summary of Findings

> The distribution of BorrowerAPR, the main variable of interest is a normal multimodal distribution. The distribution of the BorrowerRate, another variable of interest is also normal and multimodal. BorrowerRate and BorrowerAPR are highly positively correlated (0.993), which makes sense since their distributions are similar with only a slight difference since the APR is always higher than the interest rate.

> The borrower's annual percentage rate (APR) and BorrowerRate (interest rate) decreases with increasing Prosper ratings. Borrowers with the best Prosper ratings have the lowest APR and interest rates. It means that the Prosper rating has a strong effect on BorrowerAPR and BorrowerRate.

> The correlation coefficient of BorrowerAPR and LoanOriginalAmount is -0.426. Interestingly, the relationship between BorrowerAPR and loan amount turns from negative to slightly positive when the Prosper ratings are increased from HR to AA. This may be because people with higher ratings tend to borrow more money and increasing the borrower's APR could deter them from borrowing more and minimizes the business profit. However, people with lower ratings tend to borrow less money, decreasing the BorrowerAPR could encourage them to borrow more.

> The length of most loans are 36 months, followed by 60 months. There are a few 12-month termed loans. This should have a direct effect on Borrower's Rate. BorrowerAPR decreases with increasing Loan term for Self-employed, Part-time and Retired borrowers. The APR was slightly elevated for 36-month termed loans for the other employment statuses.

> The LoanOriginalAmount is positively correlated with the StatedMonthlyIncome, it makes sense since borrowers with more monthly income could loan more money. The LoanOriginalAmount is highly positively correlated with the MonthlyLoanPayment (0.916), it makes sense since borrowers tend to offset their loans by month end. The loan amount increases with increasing loan term and with increasing Prosper ratings.

> A vast majority of borrowers in each prosper rating are employed. I can infer that it is mostly the employed population that take loans.
There are more 36-month termed loans for all ProsperRatings and EmploymentStatus. Also, ProsperRating C had more counts among the Employed, Self-employed and 'Other' employment status borrowers, while ProsperRating A had more counts among the Full-time borrowers.

> The borrower's top five occupations are ‘Computer programmer’, ‘Executives’, ‘Teacher’, ‘Administrative Assistant’, and ‘Analyst’. The least borrowers are ‘Students’. Majority of loans were 36-month termed in almost all the various occupations. 

> As StatedMonthlyIncome incresases, so does the prosper ratings.

> Loan amount and Prosper ratings are the best predictors of BorrowerAPR.



## Key Insights for Presentation

> The presentation will focus on the features affects the borrower APR, which are the Loan amount and the Prosper ratings. The distributions of the BorrowerAPR, loan amount and Prosper ratings will be displayed first after which the relationships between BorrowerAPR, loan amount and ProsperRating will be displayed next. 