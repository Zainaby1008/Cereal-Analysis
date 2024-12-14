# Cereal Analysis
## Project Overview
The primary objective of this analysis is to understand the relationship between cereal attributes and consumer preferences as reflected in ratings.
This involves analyzing the nutritional content, manufacturer trends, shelf placement, and other factors to provide actionable insights for cereal manufacturers and retailers.

<br/>
![Screenshot (141)](https://github.com/user-attachments/assets/a85c923b-97b4-4250-9083-e4ffc752c607)

### Data Sources - [80 cereals.kaggle](https://www.kaggle.com/datasets/crawford/80-cereals)
### Tool - [MSSQL](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
### Data Cleaning/Preparation<br/>
-Data understanding and Inspection<br/>
-Cleaning and formatting
### Exploratory Data Analytics (EDA)
1. Which manufacturer has the healthiest cereals?
2. What is the relationship between sugar content and rating?
3. What are the key attributes of the top 5 rated cereals?
4. How does the shelf level affect cereal ratings?
5. Are higher-rated cereals more nutritious?
### Data Analytics
-Pivot tables<br/>
-For the KPIs, I used 'COUNTIFS','SUM' and so on. E.g: 'COUNT(Table1[Id])' for no of loan issued.
### Results/Findings
From the analytics, I found that:
- 53% of the loan issued are for **debt consolidation**.
- Most of the loan are issued for short term.
- Approximately 14% of the total amount of issued loans are charged off.
- Those with lower annual income are borrowing higher loan amount than those with higher annual income.
- The region with the highest loan size is the **South**.
- The default rate for verified loan is higher than that of unverified loans.
- Florida has the highest default rate (17%) and Massachusetts has the least default of 11%
  ### Recommendations
  Based on my findings, I recommend that:
- The states with lower default rates may offer insights on borrower profiles that can be applied to higher-risk areas.
- It is important to manage loans for the purpose of debt consolidation carefully as it dominates the company's portfolio.
- While the charged of rate is not excessively high, it is significant enough to warant attention and further analysis should be done on it to mitigate risks.
- The company should conduct a cost-benefit analysis to determine if the effort and cost of verification are worth it, given that unverified loans have a lower default rate. They may consider revising or optimizing the verification process.
### Limitations
Some limitations in the analysis include:

- Exclusion of outlier records with extreme loan amounts or income levels to avoid skewing results.(for example, I filtered the data to include only states with a higher number of loans (e.g., a minimum threshold of loans issued) and then analyze the default rates among those states. This ensures I am drawing insights from a dataset that's large enough to be representative.
- Assumptions in handling missing values could introduce some bias.
- Data only covers a certain period and may not fully reflect current market conditions.
