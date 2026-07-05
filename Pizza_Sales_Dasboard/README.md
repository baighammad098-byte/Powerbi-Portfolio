# Pizza Sales Report — Power BI Dashboard

A 2-page Power BI report analyzing a full year (Jan–Dec 2015) of pizza restaurant sales — covering overall sales performance and a dedicated best-seller / worst-seller breakdown.

## 📊 Overview

This project started as a SQL analysis (`sql_1st_project`) and was extended into an interactive Power BI dashboard, turning raw pizza order data into an executive-style sales report with two focused pages:

1. **Home** — overall sales performance
2. **Best / Worst Sellers** — top and bottom performing pizzas by revenue, quantity, and orders

## 🗂️ Data Model

| Table | Role |
|---|---|
| `pizza_sales` | Single fact table containing order-level pizza sales data (date, category, size, name, quantity) |

## 📐 Key DAX Measures

- **Total Revenue** — sum of sales value
- **Total Orders** — count of distinct orders
- **Total Pizzas Sold** — sum of quantity sold
- **Avg Order Value** — average revenue per order
- **Avg Orders Per Order** — average items per order
- Supporting calculated fields: **Order Month**, **Order Day**

## 📈 Page 1 — Home (Sales Performance)

- KPI cards for Total Revenue, Total Orders, Total Pizzas Sold, Avg Order Value
- Bar/column charts by **pizza category** and **pizza size**
- Trend view by **day of week** and **month**
- Callouts highlighting:
  - Classic category and Large size pizzas drive the most sales
  - Orders peak on **Friday/Saturday evenings**
  - **July and January** are the highest-order months

## 📈 Page 2 — Best / Worst Sellers

- Ranked views of pizzas by revenue, quantity sold, and total orders
- Callouts highlighting:
  - **Thai Chicken Pizza** and **Classic Deluxe Pizza** as top performers (revenue, quantity, orders)
  - **The Brie Carre Pizza** as the lowest performer across all three metrics
- Page navigation buttons to switch between Home and Best/Worst Sellers

## 🛠️ Tools Used

- **SQL** — initial data exploration and querying
- **Power BI Desktop** — data modeling, DAX measures, report design
- Fluent 2 Power BI theme

## 🚀 How to Use

1. Download `sql_1st_project.pbix` and open it in Power BI Desktop.
2. Refresh the data connection or point it to your own `pizza_sales` dataset.
3. Use the page navigator buttons to move between the Home and Best/Worst Sellers pages.
4. Use the slicers to filter by category, size, or date range.

## 👤 Author

Built by **Hammad** as part of a data analytics portfolio, combining SQL analysis with Power BI reporting and DAX.
