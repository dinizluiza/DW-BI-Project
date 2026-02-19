# Data Warehousing Project - Pizzaria Giganorme

This repository documents the final project for the Data Warehousing course of the Post-Graduation program in Computer Science at UFPE. It presents the modeling, transformation (ETL), and visualization process of a fictional pizzeria's sales data using Power BI.

**Author:** Luiza Diniz Mendes Monteiro Luna
**Year:** 2025

<img width="923" height="520" alt="Captura de tela 2026-02-19 204855" src="https://github.com/user-attachments/assets/dd85fc7b-b353-4886-9104-240e8df5cc8f" />

## 1. Data Source & Modeling
* **Source:** Four `.csv` files (`orders`, `order_details`, `pizzas`, and `pizza_types`).
* **Schema:** SnowFlake model.
* **Fact Tables:** `Fato_Pedidos` and `Fato_Detalhes_Pedido`.
* **Dimension Tables:** `Dim_Pizzas` and `Dim_Tipos_Pizzas`.

## 2. ETL Process (Power Query)
* **Standardization:** Promoted headers and translated table/column names to Portuguese.
* **Data Typing:** Changed price locale to "Brazil" to handle decimal separators correctly.
* **Time Intelligence:** Extracted Day Name and Month Name from order dates.
* **Conditional Logic:** Created conditional columns for proper sorting of days, months, and pizza sizes.
* **Merging & Calculation:** Merged tables to bring unit prices into order details and created a custom column for Total Value.

## 3. Dashboard & Visualization
* **KPIs:** Total Revenue, Average Price per Order, Total Pizzas Sold, Total Orders, and Average Pizzas per Order.
* **Dynamic Visuals:** Includes Column, Line, Funnel, and Donut charts.
* **Field Parameters:** Implemented Field Parameters to allow users to dynamically switch the X-axis of visuals (e.g., toggling between "Day of the Week" and "Month" for the top visuals, or "Size" and "Category" for the bottom visuals) without needing multiple duplicate charts.
* **Filters:** Global data slicing by Date range and Category.
