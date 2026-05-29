# Bank Statement Visualisation
The goal of this project is to take bank statements and visualise the data therein, providing insight on income versus expenses.

## Goals
The tool used for the visualisations is **Power BI**. The key questions this dashboard aims to answer are:
- What are the total expenses and income for a given period?
- What is the balance to date? Does it meet the target balance?
- What are the trends in the balance over time? Is the balance growing or shrinking overall?
- What are the top 5 expenses? Is there any possiblitiy to reduce them?
- What are the sources of income?
- Is there any trend in the monthly cash flow? Are there any particularly expense or cheap months?

## Method
The first step to this analysis is to download your bank statements. In this particular case where the data will be made publically available, I have generated mock data instead of reading a real bank statement.

### Generating the mock data.
I wrote a python routine to generate the mock data, following a typical format one might find when exporting their bank statments into a .xlsx file.

## Analysis
After constructing a dashboard, we can now answer the questions posed at the beginning:
- What are the total expenses and income for a given period?
    - We can drill down and filter by date, but for the period spanning all the data, we have an total income of £216.58K and total expenses of £205.04K.
- What is the balance to date? Does it meet the target balance?
    - Our balance to date is £15.68K, which is above our target of £10K, which we first achieved at the end of 2023 and beginning of 2024.
- What are the trends in the balance over time? Is the balance growing or shrinking overall?
    - While some months have negative income, the vast majority of months have positive income. Thus the balance is growing over time, with net positive incomes each year.
- What are the top 5 expenses? Is there any possibility to reduce them?
    - By far rent is the largest expense, constituting about a third of all expenses. The second and third largest expenses are from shopping distributed roughly equally between JD Sports and Amazon. The fourth and fifth biggest expenses are fitness related; gym membership and decathlon related.
- What are the sources of income?
    - Salary is the sole source of income.
- Is there any trend in the monthly cash flow? Are there any particularly expense or cheap months?
    - Due to a relatively steady income, most months are positive in income. Regarding expenses, it seems that the beginning of the year (Jan - May) expenses are typically lower. On average, the months June, July, and November show expenses greater than income.
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
- Do I need to spend this much money on decathlons?
- Can I get a cheaper gym membership while retaining all the facilities I need?
- In recreation:
	- Can I buy books that are second hand, rather than new from Waterstones?
	- Do I need to spend so much at Cineworld? Can I get a membership that maintains my access while being cheaper in the long run?
- In food & drink, do I need to spend this much on chains? Can I prepare food and drink at home and bring it with me? Perhaps I could set a weekly/monthly budget for this
- Are all my subscriptions necessary? Do I need to pay for both Netflix and Disney plus?