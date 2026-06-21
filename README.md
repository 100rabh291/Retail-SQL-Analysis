# Retail-SQL-Analysis
SQL-driven retail analytics using 9 queries (JOIN, GROUP BY, aggregates) to uncover profitability and discount strategy insights, visualised in Excel
# Retail Sales & Marketing Performance Analysis — SQL + Excel

## 📊 Overview
A SQL-driven analytics project querying retail transaction data to uncover profitability issues, customer value patterns, and discount strategy problems — visualised in Excel.

## 📁 Dataset
**Source:** Sample Superstore (global retail transactions dataset)
**Scope:** 9,994 transaction rows, queried via SQLite

## 🎯 Business Questions Answered
- Which product category and region perform best?
- Which sub-categories are losing money despite generating sales?
- Which states show a damaging discount-to-profit relationship?
- Who are the most valuable customers — and are the "top spenders" actually profitable?
- How do returns affect specific orders and customers?

## 🛠️ Tools & Techniques
- SQL (SQLite) — 9 queries covering:
  - `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`
  - `GROUP BY` with aggregate functions (`SUM`, `AVG`, `COUNT`, `COUNT DISTINCT`)
  - `JOIN` across two tables (orders + returns)
- Microsoft Excel for visualisation and dashboard presentation

## 🔍 Key Findings
1. **Technology** leads all categories with $8.4 lakh in sales
2. **Tables** sub-category is the biggest loss-maker — $2L+ in sales but **-$17,753** in profit
3. **Texas (37% avg discount)** and **Illinois (39%)** show the heaviest losses from over-discounting
4. **Sean Miller**, the #1 customer by sales ($25,043), is actually **loss-making** (-$1,980) — high spend doesn't always mean high value
5. **Tamara Chand** emerged as the genuinely most valuable customer — high sales AND high profit
6. **Standard Class** shipping accounts for 6,120 of all orders — nearly 3x more than the next most-used method

## 💡 Recommendations
- Urgently review discount policy on Tables, Bookcases, and Supplies
- Cap maximum allowable discount percentage in high-loss states (Texas, Illinois, Ohio)
- Investigate Sean Miller's order pattern to understand the loss-driving discount usage
- Launch loyalty incentives targeting genuinely high-value customers like Tamara Chand

## 📈 Sample Query
```sql
SELECT Sub_Category,
       ROUND(SUM(Sales), 2) AS Total_Sales,
       ROUND(SUM(Profit), 2) AS Total_Profit
FROM orders
GROUP BY Sub_Category
ORDER BY Total_Profit ASC;
```

## 👤 Author
Saurabh Shrivastava — Aspiring Data Analyst
[https://www.linkedin.com/in/saurabh-shrivastava-b4521087] | [saurabh.ns10@gmail.com]

