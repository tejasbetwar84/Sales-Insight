# Sales-Insight
Sales Insights Data Analysis Project
AIMS GRID
Purpose (Why are we doing this? (in order to ...)
To unlock Sales Insight that is not visible for before the Sales Team for decision support & automate them to reduced manual time spent in data gathering

Stakeholders (For whom are we doing this?)
Sales Director, Marketing Team, Custom Service Team, Data & Analytics Team, IT team

End Result (What do we need to achieve in the time)
An automated Dashboard providing quick & latest insights in order to support data driven decision making

Success Criteria (Against which criteria will the result be measured?)
a) Dashboard(s) uncovering sales order insights with latest data available

b) Sales Team able to take better decisions & prove 10% cost savings of total spend

c) Sales Analyst stop data gathering manually in order to save 20% of business time and reinvest it in value added activity

DATA ANALYSIS USING SQL
Show all customer records

SELECT * FROM customers;

Show total number of customers

SELECT count(*) FROM customers;

Show transactions for Chennai market (market code for chennai is Mark001)

SELECT * FROM transactions where market_code='Mark001';

Show distinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

Show transactions where currency is US dollars

SELECT * from transactions where currency="USD":

Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and (transactions.currency="INR" or transactions.currency="USD");

Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR" or transactions.currency="USD");

Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

Dashboard URL
https://public.tableau.com/app/profile/tejas.betwar/viz/SalesInsight_16605058243880/Dashboard1

