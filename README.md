# Cereal Analysis
## Project Overview
The primary objective of this analysis is to understand the relationship between cereal attributes and consumer preferences as reflected in ratings.
This involves analyzing the nutritional content, manufacturer trends, shelf placement, and other factors to provide actionable insights for cereal manufacturers and retailers.

<br/>
![Screenshot (141)](https://github.com/user-attachments/assets/a85c923b-97b4-4250-9083-e4ffc752c607)

### Data Sources - [80 cereals.kaggle](https://www.kaggle.com/datasets/crawford/80-cereals)
### Tool - [MSSQL](https://www.microsoft.com/en-us/sql-server/sql-server-downloads), [MSExcel](https://www.microsoft.com/en-us/microsoft-365/excel)
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
- Pivot tables<br/>
- For the KPIs, I used 'COUNTIFS','SUM', 'AVERAGE' and so on. E.g: 'COUNT(Table1[Id])' for no of loan issued.
 ```sql
UPDATE cereal
set "type" = case
	WHEN "type" = 'C' THEN 'Cold'
	WHEN "type" = 'H' THEN 'Hot'    
END;
--updating some columns for better understanding and easier analysis
```
```sql
select rating, sugars
from cereal;
--trying to use this to check the correlation between the rating and the sugar
```
### Results/Findings
From the analytics, I found that:
- Nabisco (N),  followed by American Home Food Products (A) have the highest average nutritional value. This indicates that these manufacturers prioritize nutrition, likely incorporating more fiber, protein, or essential vitamins into their cereals.
- As sugar content increases, the ratings tend to decrease significantly.
- The key attributes of the top rated cereals are;high fiber content,low sugar content, nutrient dense and mostly manufactured with natural ingridients.
- Consumers seem to have a preference for high fiber cereals.
- The position of cereals on shelves (1 = bottom, 2 = middle, 3 = top) does not seem to influence their consumer ratings.
- Consumers tend to rate cereals higher when they have better nutritional profiles.
  ### Recommendations
  Based on my findings, I recommend that:
- For High-Performing Manufacturers (Nabisco and American Home Food Products):<br>
Maintain Leadership: Continue to innovate with nutrient-dense cereals, emphasizing their health benefits.
- For Mid-Tier Manufacturers (Kellogg's, Post, Ralston Purina):<br>
Boost Nutritional Content: Reformulate products to include more whole grains, fiber, and vitamins.
- For Low-Performing Manufacturer (General Mills):<br>
Reassess Product Portfolio: Identify low-performing cereals in terms of nutrition and reformulate recipes to meet modern health demands.
- Retailers:<br>
Place products with higher nutritional value in premium shelf positions or health sections.
- Use terms like "whole grain," "rich in fiber," or "heart-healthy" on packaging and in advertisements to attract health-conscious consumers.
- Optimize Shelf Position for Target Audience:
1. Top Shelves (3): Target health-conscious adults with high-rated, nutrient-dense cereals.
2. Middle Shelves (2): Place cereals with broad appeal, such as family-friendly or balanced options.
3. Bottom Shelves (1): Position kid-focused or budget-friendly cereals here.

- Pricing and Positioning:Since high-rated cereals are more nutritious, they could justify premium pricing. Position these cereals on eye-level shelves to attract buyers.

### Limitations
Some limitations in the analysis include:
- The calculation of the nutritional value may not be completely accurate.
- Data only covers a certain period and may not fully reflect current market conditions.
