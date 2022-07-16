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

Regarding borrower motivations, the largest population of people seemed to have taken loans to finance previously accrued debt, rather than to start businesses or purchase assets. Debt consolidation also accounted for the highest loan amounts collected from the platform on average. Asides business purposes, borrowers seem to depend on huge loans to finance weddings, child adoptions, boat acquisitions, and the purchase of engagement rings. While all these may point to possibly self indulgent reasons, it seems that these practices are quite commonplace: see [this article from Bankrates](https://www.bankrate.com/loans/personal-loans/top-reasons-to-apply-for-personal-loan/).

In terms of the factors that may influence loan favorability. The annual percentage rate on a loan (Borrower APR) was found to be negatively correlated with the size of the loan taken, the loan term, and the rating of the borrower on the prosper platform. The Prosper rating also appeared to be a key factor on its own, influenced positively by high income from a verifiable source, a stable means of employment, homeownership, and a low debt-to-income ratio. These observations agree with a [similar article by Money Crashers](https://www.moneycrashers.com/factors-affect-personal-loan-interest-rate/) on how to secure the best APR for personal loans.

Further exploration exposes a dichotomy in the interaction between borrower APR and prosper ratings. Borrowers with low prosper ratings seemed to pay lower rates as their ratings increased on the platform. However, this pattern reverses for borrowers with higher ratings. The possible involvement of lurking variables was later discovered. It appears that high-rated borrowers may have a propensity to borrow huge sums, when long-term loans are involved. Hence, an increase in APR could be a great way to disincentivize 'overborrowing'. On the other hand, decreasing APR for long-term loans might be a great way to build capacity for low-rated borrowers, especially to take loans with enough repayment periods.

These insights are important to our story. They will be polished further through explanatory visuals.

## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.