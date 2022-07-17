# Exploring Prosper Loan Data
#### by Israel Ogunmola - July 2022

## Overview
This project aims to analyze loan data from [Prosper Marketplace](https://www.prosper.com/), a company based in San Francisco, California, that specializes in providing peer-to-peer loans at low interest rates to borrowers. The goal is to identify the different borrower motivations when applying for loans, and several factors that may influence loan favorability (measured in terms of annual percentage rates).

## Dataset
The prosper loan dataset contains information on 113,937 loans described with 81 variables. The variables included loan amount, borrower rate (or interest rate), borrower employment status, borrower income, and many others. The dataset can be found on [Udacity servers](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1554484977406000), and a detailed explanation of all its features can be obtained from [this spreadsheet](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).

## Preliminary Wrangling
Of the 81 features in the dataset, 14 were selected for exploration. Prosper rating and Borrower APR were identified as the key variables to measure loan favorability. With a concise cleaning workflow, duplicate records were removed, data types were properly converted, and null records for the key variables were dropped. State longitude and latitude information was gathered from data uploaded by GitHub user, [Rashida048](https://raw.githubusercontent.com/rashida048/Exploratory-data-Analysis-in-R/main/statelatlong.csv), to aid the visualization of loan patterns across states. At the end of the wrangling process, the original dataset had been streamlined to 83,982 loan records and 17 variables.

## Summary of Findings
The exploration process yielded a mix of both intuitive and rather unexpected results. 

The largest population of people seemed to have taken loans to finance previously accrued debt, rather than to start businesses or purchase assets. Debt consolidation also accounted for higher loan amounts than other reasons. Asides business purposes, borrowers depended on huge loans to finance weddings, child adoptions, boat acquisitions, and the purchase of engagement rings.

The annual percentage rate on a loan (Borrower APR) was negatively correlated with the loan size, the loan term, and Prosper rating. Prosper rating appeared to be a key factor on its own, influenced positively by high and verifiable incomes, stable means of employment, homeownership, and low debt-to-income ratio.

Further exploration reveals a dichotomy between borrower APR and Prosper rating. Both variables correlated negatively, up to the B rating. However, the pattern reverses after that. The possible involvement of lurking variables was discovered. High-rated borrowers may have a propensity to borrow huge sums, when long-term loans are involved. Hence, increasing APR could disincentivize 'overborrowing'. Alternatively, lowering APR for long-term loans can build capacity for low-rated borrowers.

## Key Insights for Presentation
Explanations start with the most common reasons why people borrow through prosper, and the average amounts that people borrow for those reasons. The information was conveyed using two barplots. 

Furthermore, the influence of Prosper rating on loan interest rate was explained. This used a mix of box plots, scatterplots, and point plots to show disparities in borrowing power for high and low-rated borrowers. The interesting influence of lurking variables, like loan term, was also visualized.