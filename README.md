# 🌎Billionaire-Statistics-Analysis-with-SQL-Excel🌎

## Description:
This project involves an in-depth analysis of global billionaires using a dataset that includes personal details, business information, and economic indicators. The analysis is performed using SQL for data querying and Excel for data visualization. Key insights from this project reveal patterns in wealth distribution, industry influence, demographic trends, and economic impacts across different countries.

## 🎯Key Features:

Comprehensive Dataset: Includes details such as wealth ranking, net worth, industry, age, country, and more.
SQL Queries: A variety of SQL queries are used to extract meaningful insights, such as the distribution of billionaires by country and city, gender-based wealth distribution, and top industries contributing to billionaire wealth.
Visualizations: Excel charts and graphs illustrate key findings, making complex data easily understandable.

## 🖊️Highlighted SQL Queries:

#### Total Billionaires by Country and City:

SELECT COUNT(DISTINCT country) AS country_count, COUNT(DISTINCT city) AS city_count
FROM billionaries;

#### Source-Based Wealth Distribution:

SELECT source, SUM(finalWorth) AS total_worth
FROM billionaries
GROUP BY source
ORDER BY total_worth DESC;

#### Gender Proportion of Billionaires:

SELECT gender, COUNT(*) * 100.0 / (SELECT COUNT(*) FROM billionaries) AS percentage
FROM billionaries
GROUP BY gender;

#### Top 10 Wealthiest Individuals:

SELECT personName, finalWorth
FROM billionaries
ORDER BY finalWorth DESC
LIMIT 10;

## 📊Visuals Included:

➡️Charts displaying the proportion of billionaires by gender
➡️Graphs illustrating total net worth by industry
➡️Visual representation of GDP and CPI by country

## ⛳Conclusion:
This analysis provides valuable insights into the demographics and economic impact of billionaires worldwide. By leveraging SQL and Excel, the project demonstrates how data can be transformed into actionable intelligence.


