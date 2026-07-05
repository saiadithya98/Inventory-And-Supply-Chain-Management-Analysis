# Inventory & Supply Chain Management Analysis — Power BI Dashboard

## Overview
This Power BI dashboard analyzes inventory and supply chain performance using the `Inventory_SupplyChain_Dataset.csv` dataset. The data spans multiple years (2020–2024) and includes fields such as Date, Region, Category, Supplier, Warehouse, Order Status, Units Sold, Inventory Level, Transportation Cost, Order Accuracy, Lead Time, Backorder, Cost of Goods Sold (COGS), Average Inventory, and Warehouse Capacity.

The report page includes two global slicers (**Region** and **Category**) that filter every visual on the page, plus three KPI cards and six charts.

![Full Dashboard](images/full_dashboard.png)

---

## Slicers

| Slicer | Description |
|---|---|
| **Region** | Filters all visuals by region (North, South, East, West, or All). |
| **Category** | Filters all visuals by product category (Accessories, Clothing, Electronics, Furniture, or All). |

---

## KPI Cards

### 1. Warehouse Utilization — 34.08
Shows the average warehouse utilization rate, calculated as **Average Inventory ÷ Warehouse Capacity** (expressed as a value/percentage). It indicates how much of the available warehouse capacity is currently being used to store inventory. This same metric is displayed twice on the dashboard — once as a plain KPI card and once as a gauge (below).

### 2. Day Sales of Inventory (DSI) — 15.56
Measures the average number of days it takes to sell/turn over inventory, typically calculated as **(Average Inventory / COGS) × Number of Days**. A lower value means inventory is moving faster; a higher value signals slower-moving stock.

### 3. Warehouse Utilization (Duplicate) — 34.08
A repeated KPI card for emphasis, showing the same warehouse utilization figure as Card 1.

![KPI Cards](images/kpi_cards.png)

---

## Charts

### 1. Warehouse Utilization (Gauge)
A gauge/dial visual showing warehouse utilization (34.08) against a scale of 0 to 100, with a target/reference line marked at 75.00. This gives a quick visual read on how close warehouses are to reaching a target or maximum efficient utilization level.

![Warehouse Utilization Gauge](images/gauge.png)

### 2. Sum of Transportation Cost by Region and Category (Clustered Column Chart)
A clustered bar chart comparing total transportation cost across the four regions (North, West, East, South), broken down by product category (Accessories, Clothing, Electronics, Furniture — shown in different shades of green/black). This highlights which regions and categories drive the highest shipping/logistics costs.

![Transportation Cost by Region and Category](images/transport_cost.png)

### 3. Sum of Units Sold by Year (Line/Area Chart)
A trend line showing total units sold each year from 2020 to 2024, with data labels (e.g., 55K in 2020, dipping near 0 in 2021, then rising sharply to ~192K in 2022 and ~195K in 2023–2024). This visualizes overall sales volume growth over time and highlights the recovery after a 2021 dip.

![Units Sold by Year](images/units_sold.png)

### 4. Average of Lead Time by Category (Donut Chart)
A donut chart breaking down average supplier lead time (in days) by product category: Accessories (16.60, ~26.3%), Electronics (15.29, ~24.2%), Furniture (15.50, ~24.5%), and Clothing (15.68, ~24.86%). This helps identify which product categories typically take longer to receive from suppliers.

![Average Lead Time by Category](images/lead_time.png)

### 5. Count of Backorder by Order Status (Column Chart)
A bar chart showing the count of backordered items grouped by order status: **Fulfilled** (highest, ~900+), **Pending** (~250), and **Canceled** (~150). This highlights how many orders with backorders end up fulfilled versus stuck pending or ultimately canceled — a key indicator of supply chain reliability.

![Backorder by Order Status](images/backorder.png)

### 6. Sum of Inventory Level by Category and Region (Horizontal Bar Chart)
A horizontal clustered bar chart showing total inventory levels for each product category (Clothing, Electronics, Furniture, Accessories), split by region (East, North, South, West — color coded). This shows how inventory is distributed across regions for each category, useful for spotting overstock or understock situations.

![Inventory Level by Category and Region](images/inventory_level.png)

---

## How the Visuals Work Together
- The **KPI cards and gauge** give a quick, high-level snapshot of overall warehouse efficiency and inventory turnover.
- The **Transportation Cost** and **Inventory Level** charts break down operational costs and stock distribution by region/category, useful for cost optimization and rebalancing inventory.
- The **Units Sold trend** shows the business's sales trajectory over time.
- The **Lead Time** and **Backorder** visuals together highlight supply chain reliability — how long suppliers take, and how often stockouts/backorders lead to fulfilled vs. canceled orders.

## Suggested Uses
- Filter by **Region** or **Category** to drill into performance for a specific market segment.
- Use the **Backorder by Order Status** chart alongside **Lead Time** to identify categories/suppliers causing delays.
- Compare **Transportation Cost** against **Inventory Level** by region to find cost-saving opportunities in warehousing and logistics.
