# Dynamic Retail Dashboard

## Project Objectives

The Dynamic Retail Dashboard aims to:
1. Provide a comprehensive view of key retail metrics and performance indicators.
2. Facilitate data-driven decision-making by enabling users to explore sales, profits, order quantities, and market dynamics.
3. Offer a flexible, interactive user interface for analyzing sales performance across different dimensions such as segments, categories, regions, and customer behavior.

## Significance

This dashboard serves as a powerful tool for retail businesses by enabling users to:
- Understand and optimize key sales and profit metrics.
- Identify top and bottom-performing segments, markets, and customers.
- Analyze returns, identify trends, and detect areas of improvement.
- Make strategic decisions with data-backed insights into regions and market shares.

## Data Sources

### Orders Table
| Row ID | Order ID | Returned | Order Date | Ship Date | Ship Mode | Customer ID | Customer Name | Segment | City | State | Country | Postal Code | Market | Region | Product ID | Category | Sub-Category | Product Name | Sales | Quantity | Discount | Profit | Shipping Cost | Order Priority |
|--------|----------|---------|------------|-----------|-----------|-------------|---------------|---------|------|-------|---------|-------------|--------|--------|------------|----------|--------------|--------------|-------|----------|----------|--------|---------------|---------------|
| 32298  | CA-2012-124891 | No | 31-7-2020 | 31-7-2020 | Same Day  | RH-19495 | Rick Hansen | Consumer | New York City | New York | United States | 10024 | US | East | TEC-AC-10003033 | Technology | Accessories | Plantronics CS510 - Over-the-Head monaural Wireless Headset System | 2309.65 | 7 | 0 | 762.1845 | 933.57 | Critical |
| 26341  | IN-2013-77878 | Yes | 5-2-2021  | 7-2-2021  | Second Class | JR-16210 | Justin Ritter | Corporate | Wollongong | New South Wales | Australia | | APAC | Oceania | FUR-CH-10003950 | Furniture | Chairs | Novimex Executive Leather Armchair, Black | 3709.395 | 9 | 0.1 | -288.765 | 923.63 | Critical |

### People Table
| Person           | Region   |
|------------------|----------|
| Anna Andreadi    | Central  |
| Chuck Magee      | South    |
| Kelly Williams   | East     |
| Matt Collister   | West     |

### Return Table
| Returned | Order ID        | Market        |
|----------|-----------------|---------------|
| Yes      | MX-2013-168137  | LATAM         |
| Yes      | US-2011-165316  | LATAM         |
| Yes      | ES-2013-1525878 | EU            |
| Yes      | CA-2013-118311  | United States |

## Steps to Create the Dashboard

1. **Data Import and Preparation**
   - Load the `Orders`, `People`, and `Return` tables into your chosen data visualization tool.
   - Clean and format data to ensure consistency across columns (e.g., date formats, null values).
   - Create relationships between tables based on relevant keys (e.g., `Order ID`).

2. **Create Calculated Fields**
   - Develop calculated fields to generate key metrics, such as:
     - Total Sales: `Sum([Sales])`
     - Total Profit: `Sum([Profit])`
     - Total Quantity: `Sum([Quantity])`
     - Number of Orders: `Count([Order ID])`
     - Profitability: `Sum([Profitability])`
     - Average Discount: `Average([Discount])`

<img width="395" alt="{ECE3E144-C41F-4115-AF2A-FB030D0895DE}" src="https://github.com/user-attachments/assets/27f44c87-bf60-4248-ba82-d27dba17ceb2">

3. **Building the KPI Table**
   - Add a table showcasing critical KPIs with symbols:
     | Name              | Metrics                | Symbol |
     |-------------------|------------------------|--------|
     | Total Sales       | Sum of Sales           | ㉌     |
     | Total Profit      | Sum of Profit          | 📈     |
     | Total Quantity    | Sum of Quantity        | 📦     |
     | Number of Orders  | Count of Order ID      | 🛒     |
     | Profitability     | Sum of Profitability   | 💹     |
     | Average Discount  | Average of Discount    | 🔍     |
     

4. **Create Visualizations**
   - **Charts for Segment, Category, and Market Analysis:** Bar/column charts displaying total sales, profits, and quantities broken down by segments, categories, and markets.
   - **Top 5 and Bottom 5 Analysis:** Highlight top and bottom 5 entries for sales, profits, and order quantities using bar charts.
   - **World Map Visualization:** Plot the top 10 countries by total sales on a world map to display geographic sales distribution.
   - **Market Share by Region:** Pie or doughnut charts showing market share contributions of each region.
   - **Sub-Category Contribution:** Bar charts displaying the contribution of top-performing sub-categories to overall sales.

5. **Interactivity and Filters**
   - Add filters to allow users to slice and dice data based on different dimensions like date range, market, region, segment, etc.
   - Utilize interactive elements such as slicers, drop-downs, and buttons for a dynamic user experience.

## Key Insights and Features

### Important KPIs
- Dynamic KPI table that provides a quick overview of key business metrics such as total sales, profit, and order counts.

### Charts and Visualizations
- **Segment, Category, and Market Analysis Charts** providing a clear view of performance across multiple dimensions.
  <img width="406" alt="{E0B88899-8EB4-4995-A95B-76B799D27438}" src="https://github.com/user-attachments/assets/aae23156-4039-4d4d-af93-7f956cc8b0d3">

- **Top 5 and Bottom 5 Performance** charts for focused insights into best and worst-performing categories.
  <img width="296" alt="{8FC67086-1466-4DFF-B3CD-55920B6613F1}" src="https://github.com/user-attachments/assets/025dfc88-c1d1-4863-bfd0-d64b7ce15382">

- **World Map Visualization** showcasing geographic sales distribution.
  <img width="224" alt="{86BB4039-4284-4EDE-9AF8-01A48EDBDB12}" src="https://github.com/user-attachments/assets/f9919f0b-cd0f-445a-b773-fac3448ba4dc">

- **Market Share by Region Chart** indicating market dominance and performance in specific regions.
  <img width="157" alt="{589F3199-4829-45C9-9375-B0AECC32E4AD}" src="https://github.com/user-attachments/assets/608bd139-a51a-4a33-8c9c-375fac89b6f1">


## Next Steps for Enhancement

1. **Return Analysis**: Delve deeper into analyzing returns, identifying patterns, and root causes.
2. **Top and Bottom Customer Analysis**: Understand key customers driving profits and those with the highest returns.
3. **Segment Analysis**: Explore customer segments in more depth to target marketing strategies.
4. **Market and Product Analysis**: Expand on market and product performance metrics.

## Conclusion

The Dynamic Retail Dashboard empowers businesses with actionable insights for optimized decision-making. By offering a comprehensive view of critical metrics, user-friendly visuals, and interactivity, it enables businesses to track performance, identify trends, and make data-driven decisions to enhance profitability and customer satisfaction.

<img width="759" alt="Walmart Dasboard" src="https://github.com/user-attachments/assets/faa5348b-677c-40ae-9ad2-42efe2a84f86">


