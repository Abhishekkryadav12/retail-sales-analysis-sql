# Retail Sales Analysis - SQL Project

The project cleans, explores and analyses retail transaction data using SQL, and it provides answers to real business questions concerning sales performance, customer behaviour, product categories and order timing.

## Project overview

The analysis is aimed at PostgreSQL and is based on a dataset consisting of **2,000 retail transactions** which were recorded between **January 2022 and December 2023**. This dataset includes sales from three product categories: Clothing, Beauty, and Electronics.

## Repository contents

| File | Description |
| --- | --- |
| `SQL - Retail Sales Analysis_utf .csv` | Source retail sales transaction data. |
| `sql_query_p1.sql` | Sets up the database, checks data quality, runs exploratory queries, and carries out business analysis queries. |

## Dataset columns

| Column | Description |
| --- | --- |
| `transaction_id` | Unique ID for each transaction. |
| sale_date | The date on which the sale took place. |
| sale_time | The time at which the sale takes place. |
| `customer_id` | Unique number that identifies a customer. |
| `gender` | Customer gender. |
| `age` | Customer age. |
| `category` | Product type. |
| quantity | The number of units that were purchased. |
| `price_per_unit` | Price for one unit. |
| cogs | The cost of goods sold. |
| `total_sale` | Total amount of the transaction. |

Note that when importing the file you should map `transactions_id` and `quantiy` to `transaction_id` and `quantity`.

## Database setup

1. Make a PostgreSQL database.

```sql
CREATE DATABASE sql_project_p2;
```

2. Establish a connection to sql_project_p2 and execute the table-creation section in the file sql_query_p1.sql.

3. Import the file SQL - Retail Sales Analysis_utf .csv into the retail_sales table and make sure that the two CSV header names mentioned above are assigned to the corresponding table columns.

4. Carry out the data cleaning, exploration and analysis by executing the remaining statements in the file sql_query_p1.sql.

## Analysis performed

The SQL script answers the following business questions:

1. Get all sales from a certain date.
2. Identify the clothing transactions from November 2022 that had qualifying quantities.
3. Work out the total sales and the number of orders by product category.
4. Calculate the average age of the customers in the Beauty category.
5. Find transactions over 1,000 that are especially important.
6. Count the number of transactions by gender and by category.
7. Determine, for each year, the month that has the highest average sale value.
8. Find the five customers who have spent the most in total.
9. Count the number of unique customers in each product category.
10. Divide the orders into morning, afternoon, and evening shifts and then count the orders for each shift.

## Data-quality checks

Before carrying out the analysis, the script looks for any missing values in the key transaction fields and includes a query to eliminate the incomplete records. It also examines the total number of transactions, the number of unique customers, and the available categories.

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
