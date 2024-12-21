

# Dynamic Retail Dashboard
Certainly! Below is an expanded **README** for your **Dynamic Retail Dashboard**, now including **steps to solve each problem statement** along with the data samples and other details. This will give a step-by-step guide on how each problem statement was addressed in the dashboard.

---

# Dynamic Retail Dashboard

## Overview

The **Dynamic Retail Dashboard** is a comprehensive, Excel-based solution that analyzes retail performance and provides actionable insights. Using data from three key tables—**Orders**, **Returns**, and **People**—the dashboard leverages Excel’s Power Query, PivotTables, and dynamic charts to create an interactive and flexible data model.

This dashboard aims to solve business problems and help make data-driven decisions by displaying real-time data visualizations and KPIs such as sales, profit margins, top categories, and more.

---

## Data Sources

The dashboard integrates data from three main tables, all hosted on GitHub:

- **Orders Table**: Contains transactional data, such as order IDs, customer details, product categories, sales, profit, and more.
- **Returns Table**: Contains data related to returned orders and their associated markets.
- **People Table**: Contains data about employees or stakeholders and the regions they cover.

### Sample Data for Orders Table:

| Order ID        | Returned | Order Date | Ship Date  | Ship Mode   | Customer ID | Customer Name | Segment      | City             | State/Province   | Country        | Postal Code | Region | Product ID    | Category    | Sub-Category    | Product Description | Sales    | Quantity | Discount | Profit   | Profit Margin | Priority |
|-----------------|----------|------------|------------|-------------|-------------|---------------|--------------|------------------|------------------|----------------|-------------|--------|---------------|-------------|-----------------|---------------------|----------|----------|----------|----------|---------------|----------|
| CA-2012-124891  | No       | 31-07-2020 | 31-07-2020 | Same Day    | RH-19495    | Rick Hansen   | Consumer    | New York City    | New York        | United States  | 10024       | US     | TEC-AC-10003033 | Technology | Accessories     | Plantronics CS510 - Over-the-Head monaural Wireless Headset System | 2309.65 | 7        | 0        | 762.18   | 933.57        | Critical |
| IN-2013-77878   | Yes      | 05-02-2021 | 07-02-2021 | Second Class| JR-16210    | Justin Ritter | Corporate   | Wollongong       | New South Wales | Australia      |             | APAC   | FUR-CH-10003950 | Furniture  | Chairs          | Novimex Executive Leather Armchair, Black | 3709.40 | 9        | 0.1      | -288.77  | 923.63        | Critical |

---

### Sample Data for Returns Table:

| Returned | Order ID        | Market      |
|----------|-----------------|-------------|
| Yes      | MX-2013-168137  | LATAM       |
| Yes      | US-2011-165316  | LATAM       |
| Yes      | ES-2013-1525878 | EU          |
| Yes      | CA-2013-118311  | United States|

---

### Sample Data for People Table:

| Person            | Region         |
|-------------------|----------------|
| Anna Andreadi     | Central        |
| Chuck Magee       | South          |
| Kelly Williams    | East           |
| Matt Collister    | West           |
| Deborah Brumfield | Africa         |

---

## Problem Statements and Solutions

### Problem 1: **KPI Metrics** - Total Sales, Total Profit, Quantity, Number of Orders, Profit Margin

#### Steps to Solve:
1. **Data Aggregation**: 
   - Use **Power Query** to load the **Orders** table and ensure that sales, profit, quantity, and orders are summed up for all records.
   
2. **KPI Calculation**:
   - Create calculated columns or measures in **Excel** to compute the required KPIs:
     - **Total Sales**: `SUM(Sales)`
     - **Total Profit**: `SUM(Profit)`
     - **Total Quantity**: `SUM(Quantity)`
     - **Number of Orders**: `COUNT(Order ID)`
     - **Profit Margin**: `Profit/Sales` for each order.

3. **Display KPIs**:
   - Insert **text boxes** or **cards** to display these KPIs dynamically.
   - Use **Conditional Formatting** to highlight the values (e.g., use colors for high/low values).
   
4. **Interactivity**:
   - Add slicers for **regions**, **time periods**, or **product categories** so that users can filter data and see dynamic changes in KPIs.

![image](https://github.com/user-attachments/assets/6ffa0561-a36a-49fa-8189-9bec57127fb4)

---

### Problem 2: **Sales and Profit Analysis**

#### Steps to Solve:
1. **Data Grouping**: 
   - Group the sales and profit data by **product category**, **region**, or **time period** (e.g., monthly).
   
2. **PivotTable Creation**:
   - Use **PivotTables** to summarize sales and profit values by **Category**, **Region**, or **Segment**.

3. **Charting**:
   - Create **bar charts** or **line charts** to visualize sales and profit over time or by region.

4. **Trend Analysis**:
   - Include a trend line to help identify sales and profit fluctuations, revealing patterns or seasonality.

![image](https://github.com/user-attachments/assets/af26e1cf-dce7-40f6-88e0-3bf306e7ab07)

---

### Problem 3: **Category-Wise Profit Analysis**

#### Steps to Solve:
1. **Data Preparation**: 
   - Ensure that each order is classified by its **category** in the **Orders** table.
   
2. **Summing Profit by Category**:
   - Use **PivotTables** to calculate the total profit for each **category**.
   
3. **Visualizing Profit**:
   - Create a **bar chart** or **pie chart** to represent **profit by category**, making it easy to see which categories are the most profitable.

  ![image](https://github.com/user-attachments/assets/c15ab068-767d-47c2-8d7e-3c2e37ddd97d)




---

### Problem 4: **Segment-Wise Sales Share Percentage**

#### Steps to Solve:
1. **Segment Grouping**: 
   - Group the data by **Customer Segment** (e.g., Consumer, Corporate).
   
2. **Calculate Sales Share**:
   - Use **PivotTables** to calculate the total sales for each segment.
   - Calculate the sales percentage for each segment using the formula: `Segment Sales / Total Sales`.

3. **Visual Representation**:
   - Use a **pie chart** or **stacked bar chart** to represent each segment’s contribution to total sales.
  
![image](https://github.com/user-attachments/assets/c30fb024-6a42-4046-84c6-e0c8a1e01d39)



---

### Problem 5: **Sales by Country**

#### Steps to Solve:
1. **Data Grouping**: 
   - Group sales by **Country**.
   
2. **Summing Sales**:
   - Use **PivotTables** to sum sales for each country.
   
3. **Map Visualization**:
   - If desired, use Excel’s **Map Chart** feature to visualize the sales distribution by country.
  
![image](https://github.com/user-attachments/assets/b452e524-bed6-41ee-b041-9afa57144458)


---

### Problem 6: **Top 5 Categories**

#### Steps to Solve:
1. **Ranking Categories**:
   - Use **PivotTables** to rank categories based on total **sales** or **profit**.
   
2. **Limiting to Top 5**:
   - Use the **Top 10 Filter** in the **PivotTable** to limit the view to the top 5 categories.
   
3. **Visualizing**:
   - Display the results in a **bar chart** or **column chart** that dynamically updates based on filters.

![image](https://github.com/user-attachments/assets/809b5f67-bf30-4eeb-aea1-6d223fcaaa4e)




---

### Problem 7: **Bottom 5 Categories**

#### Steps to Solve:
1. **Ranking Categories**:
   - Similar to the top categories, use a **PivotTable** to rank categories based on sales or profit.
   
2. **Limiting to Bottom 5**:
   - Use a **bottom 5 filter** in the **PivotTable** to view the least-performing categories.

3. **Visualizing**:
   - Display the results in a **bar chart** or **column chart** for clear comparison.
  
   ![image](https://github.com/user-attachments/assets/c9ee9194-5777-4905-a14a-b0f9222a9622)


---

### Problem 8: **Early Sales Trend**

#### Steps to Solve:
1. **Data Aggregation**:
   - Aggregate the data by **date** (e.g., monthly or quarterly).
   
2. **Line Chart Creation**:
   - Use a **line chart** to display the sales trend over time, highlighting periods of growth or decline.

3. **Adding Trend Line**:
   - Optionally, add a **trend line** to the line chart to visually show overall performance trends.
  
   ![image](https://github.com/user-attachments/assets/f75f1735-9703-46f7-8f51-c6c008f34487)


---

## Data Transformation and Preparation

### Power Query Editor

The data was cleaned and transformed using **Power Query** to ensure consistency and reliability before any analysis or reporting.

1. **Data Import**:
   - The data from GitHub repositories (Orders, Returns, People) was imported using **Power Query**.

2. **Cleaning**:
   - Missing values were addressed, irrelevant rows were removed, and columns were renamed for clarity.

3. **Merging Tables**:
   - The **Orders**, **Returns**, and **People** tables were merged to create a unified data model, linking them through **Order ID** and **Customer ID**.

4. **Calculated Columns**:
   - New columns like **Profit Margin** and **Return Rate** were calculated using Excel formulas.

5. **Filtering**:
   - Filters were applied to remove any outliers or irrelevant data points, ensuring the analysis was accurate.

---

## Conclusion

This **Dynamic Retail Dashboard** solves critical business problems through interactive and real-time analysis. By leveraging Excel's advanced features like Power Query, PivotTables, and dynamic charts, this dashboard provides insights into sales, profits, and customer behavior. With future enhancements, the dashboard can be expanded to include further analyses such as **Return Analysis**, **Customer Segmentation**, and **Product Performance**.


![image](https://github.com/user-attachments/assets/86a36ade-0c55-4756-8845-37d27026f319)

---

