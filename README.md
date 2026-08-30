# Retail Sales Analysis - SQL Project

This project uses SQL to clean, explore, and analyze retail transaction data. It answers practical business questions about sales performance, customer behavior, product categories, and order timing.

## Project overview

The analysis is written for PostgreSQL and uses a dataset of **2,000 retail transactions** recorded between **January 2022 and December 2023**. The dataset contains sales from three product categories: Clothing, Beauty, and Electronics.

## Repository contents

| File | Description |
| --- | --- |
| `SQL - Retail Sales Analysis_utf .csv` | Source retail transaction dataset. |
| `sql_query_p1.sql` | Database setup, data-quality checks, exploratory queries, and business analysis queries. |

## Dataset columns

| Column | Description |
| --- | --- |
| `transaction_id` | Unique identifier for each transaction. |
| `sale_date` | Date of the sale. |
| `sale_time` | Time of the sale. |
| `customer_id` | Unique customer identifier. |
| `gender` | Customer gender. |
| `age` | Customer age. |
| `category` | Product category. |
| `quantity` | Number of units purchased. |
| `price_per_unit` | Price for one unit. |
| `cogs` | Cost of goods sold. |
| `total_sale` | Total transaction amount. |

> Note: the CSV header uses `transactions_id` and `quantiy`; map these to `transaction_id` and `quantity` when importing the file.

## Database setup

1. Create a PostgreSQL database:

```sql
CREATE DATABASE sql_project_p2;
```

2. Connect to `sql_project_p2` and run the table-creation section in `sql_query_p1.sql`.

3. Import `SQL - Retail Sales Analysis_utf .csv` into the `retail_sales` table. Ensure the two CSV header names noted above are mapped to the table column names.

4. Run the remaining statements in `sql_query_p1.sql` to perform data cleaning, exploration, and analysis.

## Analysis performed

The SQL script answers the following business questions:

1. Retrieve all sales made on a specific date.
2. Find Clothing transactions in November 2022 with qualifying quantities.
3. Calculate total sales and order count by product category.
4. Find the average age of Beauty-category customers.
5. Identify high-value transactions above 1,000.
6. Count transactions by gender and category.
7. Find the best-selling month in each year based on average sale value.
8. Identify the top five customers by total spending.
9. Count unique customers in each product category.
10. Classify orders into Morning, Afternoon, and Evening shifts and count each shift's orders.

## Data-quality checks

Before analysis, the script checks for missing values in key transaction fields and includes a query to remove incomplete records. It also explores total transaction count, unique customers, and available categories.

## Dataset snapshot

- Transactions: 2,000
- Unique customers: 155
- Categories: Clothing, Beauty, Electronics
- Total recorded sales: 911,720
- Date range: 2022-01-01 to 2023-12-31

## Tools used

- PostgreSQL
- SQL
- CSV dataset

## Author

Abhii
