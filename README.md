# README
## Introduction
While we may feel that we have an intuitive feeling of where our money is going, whether it is income or outgoing, often we do not. It can be difficult to mentally quantify whether small regular expenses are comparable to large infrequent ones.

This personal finance dashboard aims to make clear spending and income habits, allowing for quantitative identification of significant expenditures that can be reduced. Similarly it may highlight expenses that are negligible to the total expenditure, making their reduction have little impact to the total outgoings.

This visualisation was done with Power BI due its efficiency in generating varied graphics and allowing exploration trends in the data.

Through this dashboard, I have identified the most significant expenses, and strategies to reduce them where possible. Due to a relatively consistent income, and monotonically increasing rent (which is by far the biggest expense), between 2020 and 2024, the account balance is increasing over time. After this, it then levels off and decrease
The goal of this project is to take bank statements and visualise the data therein, providing insight on income versus expenses.

## Goals
The tool used for the visualisations is **Power BI**. The key questions this dashboard aims to answer are:
- What are the total expenses and income for a given period?
- What is the balance to date? Does it meet the target balance?
- What are the trends in the balance over time? Is the balance growing or shrinking overall?
- What are the top 5 expenses? Is there any possibility to reduce them?
- What are the sources of income?
- Is there any trend in the monthly cash flow? Are there any particularly expense or cheap months?

## Method
The first step to this analysis is to download your bank statements. The format can be different for different banks. For my case, the bank statement was exported as a CSV file in long format, with columns:
1. date
2. transaction
3. money in
4. money out
5. balance
Because the transaction information is usually verbose, containing payment type, vendor, date, and references, it is impossible to do any analysis in its raw form. To normalise the records, a keyword based mapping table was used to translate the raw transaction descriptions into concise, standardised names. I also included a category corresponding to each merchant that allows grouping for expenses such as groceries from different merchants.

This pipeline is not generalised to be used for an arbitrary bank, and will need editing to handle different formats of bank statements.

### Mock data set
For the purposes of publishing this project, I withdrew any personal information and opted to generate a mock data set in python.

## Analysis
After constructing a dashboard, we can now answer the questions posed at the beginning:
- What are the total expenses and income for a given period?
    - We can drill down and filter by date, but for the period spanning all the data, we have an total income of £217.05K and total expenses of £212.78K.
- What is the balance to date? Does it meet the target balance?
    - Our balance to date is £10.06K, which is just above our target of £10K, which we first achieved in July 2023.
- What are the trends in the balance over time? Is the balance growing or shrinking overall?
    - On average, the net income is positive each year. While the net cash flow in July is negative, it is relatively small and not indicative of spending habits. November and December however are decidedly the most expense months, seeing significant negative cash flow.
- What are the top 5 expenses? Is there any possibility to reduce them?
    - By far rent is the largest expense, constituting about a third of all expenses. The second and third largest expenses are from shopping distributed roughly equally between JD Sports and Amazon. The fourth and fifth biggest expenses are fitness related; gym membership and decathlon expenses.
- What are the sources of income?
    - Salary comprises 99% of the total income, with the remaining 1% coming from interest.
- Is there any trend in the monthly cash flow? Are there any particularly expense or cheap months?
    - Due to a relatively steady income, most months are positive in income. On average Jan, Mar, May, July, Aug, and Oct all have very small margins where the net cash flow is almost 0. November and December see the most significant expenditure with average cash flows of -£3,337.40, and -£4.968.03, respectively.
### Expenses
Comparing the essential and non-essential expenses, 60% of expenses we essential with the remaining 40% being non-essential. Below is breakdown of some of the findings and possible strategies of reducing expenses by highlighting key areas where expenses are highest.
#### Essential expenses:
- Housing
- Utilities
- Groceries
- Transport
58% of all essential expenses comprised rent, 21% comprised utility bills, and the remaining 21% of essential expenses went to groceries and transport. It is likely that all these costs are reasonably well optimised already, meaning that there is little that is actionable. Questions that could be asked, in order of importance are:
	- Is my rent exceptionally low/high for the type of housing?
	- Are my utilities overkill for me? (paying extra for super-fast broadband when not needed)
	- Can I change my primary transport? (driving vs. using a bike)
	- Can I buy more of my groceries from cheaper supermarkets?
#### Non-essential expenses:
- Shopping
- Fitness
- Recreation
- Food & Drink
- Subscriptions
Nearly 50% (47.6%) of all non-essential expenses are spent on general shopping (Amazon, JD Sports, Currys). Almost a quarter (23.4%) of non-essential spending goes on fitness related expenses, with just over 50% of that being on Decathlon related expenses. The remaining quarter of non-essential expenses goes on recreation, food & drink, and subscriptions. Questions that can be asked to minimise non-essential spending in order of importance are:
	- Do I need to spend so much on clothes and general shopping? If so, can I sell old clothes/items that I no longer need?
	- Do I need to spend this much money at decathlon?
	- Can I get a cheaper gym membership while retaining all the facilities I need?
- In recreation:
	- Can I buy books that are second hand, rather than new from Waterstones?
	- Do I need to spend so much at Cineworld? Can I get a membership that maintains my access while being cheaper in the long run?
	- In food & drink, do I need to spend this much on chains? Can I prepare food and drink at home and bring it with me? Perhaps I could set a weekly/monthly budget for this
	- Are all my subscriptions necessary? Do I need to pay for both Netflix and Disney plus?
## Tools used
- Python (pandas) to generate a mock list of transactions
- Power BI to create all visualisations
### Requirements
- Python
	- Pandas
	- random
	- datetime
- Power BI