This is a Data Analysis Project performed on SQL & PowerBI - Part of my journey into Data Analytics

### About this Project:
- Project example provided by <code>[codebasics](https://www.youtube.com/playlist?list=PLeo1K3hjS3uva8pk1FI3iK9kCOKQdz1I9)</code>
- Data Analysis project - India based company sales insights.
- Use of SQL for ETL mapping in order to gather unstructred data to conduct data cleaning and design schema data models on PowerBi
- Develop a PowerBi dashboard for analysis and quantitative visuals to infer insights based on different parameters that may affect the company's performance on a yearly basis and provide solutions.

### Data Analysis Using SQL
1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`

### Data Analysis Using PowerBi

#### Star Schemia in PowerBi

<p align="center"><a><img width="80% src="images/si%20schema.PNG"/></a></p> >

#### PowerBi Dashboard

<p align="center"><a><img width="80% src="images/si%20dashboard.PNG"/></a></p> >
