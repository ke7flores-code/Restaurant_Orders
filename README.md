# READ ME for Restaurant Order Analysis using MySQL

## Project Overview

This project explores restaurant menu and order data using **MySQL Workbench** to identify patterns in menu pricing, customer ordering behavior, and high-value orders.

The goal was to use SQL queries to investigate the restaurant's menu, compare cuisine categories, identify popular and less popular menu items, and examine orders with the highest total item prices. The findings provide examples of how SQL can help transform raw restaurant data into useful business insights.

## Tools & Technologies

- **MySQL** — database creation, querying, and data analysis
- **MySQL Workbench** — SQL development and query execution
- **CSV** — source data and supporting documentation

## Dataset Overview

The project uses two relational tables containing restaurant menu and order information.

| Table | Description |
|---|---|
| `menu_items` | Contains menu item IDs, item names, cuisine categories, and prices. |
| `order_details` | Contains order-detail IDs, order IDs, order dates, order times, and menu item IDs. |

The dataset contains:
- **32 menu items**
- **12,234 order-detail records**
- **5,370 distinct orders**
- Four menu categories: American, Asian, Italian, and Mexican
- Order dates spanning January 1 through March 31, 2023

A data dictionary is included to explain the fields in each table.

## Business Questions

The SQL analysis investigates the following questions:

1. How many items are on the menu?
2. Which menu items have the lowest and highest prices?
3. How many menu items belong to each cuisine category?
4. What is the average menu price for each category?
5. How many orders and order-detail records are in the dataset?
6. Which orders contain the greatest number of items?
7. Which menu items are ordered most and least frequently?
8. Which five orders have the highest total menu-item prices?
9. What menu categories appear in the highest-spending orders?

## SQL Skills Demonstrated

This project demonstrates practical SQL querying and relational data analysis, including:

- `SELECT` — retrieving data from tables
- `WHERE` — filtering records based on conditions
- `ORDER BY` and `LIMIT` — sorting results and identifying top records
- `COUNT()`, `AVG()`, and `SUM()` — calculating counts, averages, and totals
- `GROUP BY` — summarizing data by menu category, item, and order
- `HAVING` — filtering grouped results
- `JOIN` — combining menu and order information using related item IDs
- `DISTINCT` — counting unique orders
- Subqueries — identifying orders containing more than a specified number of items

## Key Findings

### 1. Menu Pricing

- **Cheapest menu item:** Edamame at $5.00.
- **Most expensive menu item:** Shrimp Scampi at $19.95.
- **Most expensive cuisine category by average menu price:** Italian, averaging $16.75 per item.
- **Lowest average menu price:** American, averaging $10.07 per item.

### 2. Menu Item Popularity

- **Most frequently ordered item:** Hamburger, appearing in 622 order-detail records.
- **Least frequently ordered item:** Chicken Tacos, appearing in 123 order-detail records.

These results show differences in item-level ordering frequency that could help guide further menu performance analysis.

### 3. High-Spending Orders

The five highest-spending orders identified in the analysis were:

| Order ID | Total menu-item price |
|---:|---:|
| 440 | $192.15 |
| 2075 | $191.05 |
| 1957 | $190.10 |
| 330 | $189.70 |
| 2675 | $185.10 |

Order 440 had the highest calculated total. A category-level breakdown of these five orders showed that Italian dishes were particularly prominent in Order 440.

*Note: These totals are calculated by summing the listed menu prices for each order. They should not be interpreted as verified revenue or actual customer spending because the dataset does not establish discounts, taxes, or other adjustments.*

## Business Recommendations

Based on the analysis, several areas merit further investigation:

- **Review popular menu items:** Evaluate frequently ordered items such as hamburgers to understand their contribution to overall menu performance.
- **Investigate less frequently ordered items:** Explore whether items such as Chicken Tacos could benefit from menu placement changes, promotion, or further customer feedback.
- **Examine Italian menu performance:** Consider the category's higher average prices when reviewing menu pricing and profitability. Actual profitability would require ingredient costs and other expense data.
- **Analyze high-value orders:** Investigate combinations of items purchased in the highest-value orders to identify potential opportunities for menu bundles or complementary recommendations.

These are preliminary recommendations based on the available data rather than conclusions about profitability or customer preferences.

## Repository Contents

| File | Description |
|---|---|
| `create_restaurant_db_queries.sql` | SQL script containing database/table setup code, sample data inserts, and analysis queries. |
| `menu_items.csv` | Menu item data, including names, categories, and prices. |
| `order_details.csv` | Order-level item records, dates, times, and item IDs. |
| `restaurant_db_data_dictionary.csv` | Definitions of the fields in both tables. |
| `README.md` | Project overview, methodology, findings, and documentation. |

## How to Run the Project

1. Install and open MySQL Workbench.
2. Open `create_restaurant_db_queries.sql`.
3. Review the database creation and data-loading section. Ensure the schema, table creation, and insert statements are active SQL rather than commented-out code before attempting to execute them.
4. Execute the setup statements to create and populate the `restaurant_db` schema.
5. Run the analysis queries individually or in sections.
6. Review the query results to explore menu pricing, order frequency, and high-spending orders.

The CSV files are provided as supporting datasets and documentation.

## Project Purpose

This project represents hands-on practice in SQL-based data analysis, relational table joins, aggregation, and business-oriented interpretation of query results. It demonstrates how structured restaurant data can be explored to answer practical questions about menu performance and ordering activity.

**Author:** Kevin Flores

**Tools:** MySQL · MySQL Workbench · SQL
