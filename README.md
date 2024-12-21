

# Dynamic Retail Dashboard

## Overview

The **Dynamic Retail Dashboard** is an interactive Excel-based solution designed to provide comprehensive insights into retail business operations. The dashboard is connected to three key data tables—**Orders**, **Returns**, and **People**—which are hosted on GitHub. Using Excel's Power Query Editor, the data is loaded, transformed, and visualized in a dynamic manner, offering a holistic view of key business metrics.

The dashboard provides dynamic charts and KPIs, enabling users to analyze sales, profit margins, customer trends, and more. It is a powerful tool for business decision-making, allowing stakeholders to monitor and assess performance across various dimensions like product categories, regions, and customer segments.

---

## Data Sources

The data used in the dashboard comes from three primary tables, which are loaded into Excel from a GitHub repository. Here is a description of each table, along with a **sample of the data**:

### 1. **Orders Table**

This table contains transactional data, including order ID, product category, sales, quantity, profit, and regional details.

#### Sample Data for Orders Table:

| Order ID        | Returned | Order Date | Ship Date  | Ship Mode   | Customer ID | Customer Name | Segment      | City             | State/Province   | Country        | Postal Code | Region | Product ID    | Category    | Sub-Category    | Product Description | Sales    | Quantity | Discount | Profit   | Profit Margin | Priority |
|-----------------|----------|------------|------------|-------------|-------------|---------------|--------------|------------------|------------------|----------------|-------------|--------|---------------|-------------|-----------------|---------------------|----------|----------|----------|----------|---------------|----------|
| CA-2012-124891  | No       | 31-07-2020 | 31-07-2020 | Same Day    | RH-19495    | Rick Hansen   | Consumer    | New York City    | New York        | United States  | 10024       | US     | TEC-AC-10003033 | Technology | Accessories     | Plantronics CS510 - Over-the-Head monaural Wireless Headset System | 2309.65 | 7        | 0        | 762.18   | 933.57        | Critical |
| IN-2013-77878   | Yes      | 05-02-2021 | 07-02-2021 | Second Class| JR-16210    | Justin Ritter | Corporate   | Wollongong       | New South Wales | Australia      |             | APAC   | FUR-CH-10003950 | Furniture  | Chairs          | Novimex Executive Leather Armchair, Black | 3709.40 | 9        | 0.1      | -288.77  | 923.63        | Critical |
| IN-2013-71249   | No       | 17-10-2021 | 18-10-2021 | First Class | CR-12730    | Craig Reiter  | Consumer    | Brisbane         | Queensland       | Australia      |             | APAC   | TEC-PH-10004664 | Technology | Phones          | Nokia Smart Phone, with Caller ID | 5175.17 | 9        | 0.1      | 919.97   | 915.49        | Medium   |
| ES-2013-1579342 | No       | 28-01-2021 | 30-01-2021 | First Class | KM-16375    | Katherine Murray | Home Office | Berlin           | Berlin           | Germany        |             | EU     | TEC-PH-10004583 | Technology | Phones          | Motorola Smart Phone, Cordless | 2892.51 | 5        | 0.1      | -96.54   | 910.16        | Medium   |

---

### 2. **Returns Table**

This table provides information on returned orders, such as order ID and market region.

#### Sample Data for Returns Table:

| Returned | Order ID        | Market      |
|----------|-----------------|-------------|
| Yes      | MX-2013-168137  | LATAM       |
| Yes      | US-2011-165316  | LATAM       |
| Yes      | ES-2013-1525878 | EU          |
| Yes      | CA-2013-118311  | United States|
| Yes      | ES-2011-1276768 | EU          |
| Yes      | MX-2013-131247  | LATAM       |
| Yes      | ID-2011-20975   | APAC        |
| Yes      | IN-2014-58460   | APAC        |
| Yes      | ES-2011-3028321 | EU          |
| Yes      | MX-2014-148285  | LATAM       |

---

### 3. **People Table**

This table includes information about employees or stakeholders, such as their names and the regions they are associated with.

#### Sample Data for People Table:

| Person            | Region         |
|-------------------|----------------|
| Anna Andreadi     | Central        |
| Chuck Magee       | South          |
| Kelly Williams    | East           |
| Matt Collister    | West           |
| Deborah Brumfield | Africa         |
| Larry Hughes      | AMEA           |
| Nicole Hansen     | Canada         |
| Giulietta Dortch  | Caribbean      |
| Nora Preis        | Central Asia   |
| Jack Lebron       | North          |

---

## Dashboard Features

### KPIs and Metrics

The dashboard includes several Key Performance Indicators (KPIs) that provide an at-a-glance view of the business's performance:

| KPI                      | Name            | Symbol |
|--------------------------|-----------------|--------|
| Count of Order ID         | Total Sales     | 💰     |
| Sum of Profit             | Total Profit    | 📈     |
| Sum of Quantity           | Total Quantity  | 📦     |
| Sum of Sales              | Total Orders    | 🛒     |
| Sum of Profitability      | Profitability   | 💹     |

These KPIs are dynamic and linked to the underlying data. They update automatically based on the filters or selections made in the dashboard.

---

### Problem Statements Solved

The dashboard answers the following business questions, with corresponding visuals provided for each problem statement:

#### 1. **KPI Metrics**: Total Sales, Total Profit, Quantity, Number of Orders, Profit Margin

- **Description**: Displays the overall performance of the business through key metrics like total sales, total profit, quantity of items sold, and the number of orders.
- **Visuals**: KPIs are displayed with clear and dynamic visual indicators (e.g., bar charts, numbers with symbols) to represent the metrics in real-time.

#### 2. **Sales and Profit Analysis**

- **Description**: Provides an in-depth analysis of sales performance and profit margins across different periods and categories.
- **Visuals**: Line charts and bar charts showing sales and profit trends, along with the ability to filter by date or region.

#### 3. **Category-Wise Profit Analysis**

- **Description**: Analyzes profit for each product category to identify which categories are driving profitability.
- **Visuals**: A pie chart or bar chart visualizing profits by category, allowing users to identify high- and low-profit categories.

#### 4. **Segment-Wise Sales Share Percentage**

- **Description**: Breaks down the sales share by customer segments (e.g., Consumer, Corporate, Home Office) and presents the data in percentage terms.
- **Visuals**: Stacked bar charts or pie charts showing sales distribution across various segments.

#### 5. **Sales by Country**

- **Description**: Visualizes sales performance across different countries to identify geographical trends.
- **Visuals**: A map chart or bar graph displaying sales by country, allowing the user to drill down into regional performance.

#### 6. **Top 5 Categories**

- **Description**: Identifies and ranks the top 5 categories based on sales, profit, or other metrics.
- **Visuals**: A dynamic bar chart or table displaying the top 5 categories based on the selected metric.

#### 7. **Bottom 5 Categories**

- **Description**: Displays the bottom 5 categories based on sales, profit, or other key metrics, helping identify underperforming products.
- **Visuals**: A dynamic bar chart or table showing the least-performing categories.

#### 8. **Early Sales Trend**

- **Description**: Displays a trend line of sales over a specific time period to visualize the early trends in sales performance.
- **Visuals**: A line chart showing sales data for the earliest months or years of data, allowing businesses to assess historical growth patterns.

---

## Data Transformation and Preparation

### Power Query Editor

Before building the dashboard, Power Query Editor was used to perform several transformations on the data:

1. **Loading the Data**: The data tables from GitHub were linked to the Excel file and loaded using Power Query.
2. **Data Cleaning**: Invalid or missing values were handled, ensuring that only relevant data was included in the analysis.
3. **Data Merging**: The Orders, Returns, and People tables were merged to create a single data model for easy reporting and analysis.
4. **Creating Relationships**: Appropriate relationships between tables were established to allow for cross-table analysis.
5. **Column Creation**: New calculated columns (e.g., Profit Margin) were added to enhance the analysis.
6. **Filtering**: Only relevant data was filtered based on business needs (e.g., excluding cancelled orders).

These transformations were necessary to ensure the data was clean, structured, and ready for analysis.

---

## Dashboard Construction

### Step 1: Data Collection
- Data was fetched from GitHub repositories containing the **Orders**, **People**, and **Returns** tables. These datasets were imported into Excel and linked using Power Query.

### Step 2: Data Transformation
- Using Power Query, the data was transformed into a usable format. Unnecessary rows were removed, data was cleaned (e.g., handling missing values), and new calculated columns were created, such as **Profit Margin** and **Total Sales**.

### Step 3: KPI Definition
- Key metrics like **Total Sales**, **Total Profit**, **Total Quantity**, **Number of Orders**, and

 **Profitability** were defined using Excel formulas. These KPIs were designed to reflect the most critical aspects of business performance.

### Step 4: Visualizations
- Various charts were created, such as:
  - **Bar and line charts** to track sales and profit trends.
  - **Pie charts** for category-wise sales and profit breakdown.
  - **Dynamic slicers** to filter data by product, region, or time.
- Each chart was designed to be dynamic, updating automatically based on user input.

### Step 5: Dashboard Interactivity
- Slicers and filters were added to make the dashboard interactive. Users can select regions, time periods, and product categories to view specific metrics and performance details.
- The dashboard is updated automatically based on the selections made by users.

---

## Data Dictionary

### Orders Table

| Column Name | Description |
|-------------|-------------|
| **Order ID** | Unique identifier for each order |
| **Product** | Name or ID of the product ordered |
| **Category** | Category of the product (e.g., Technology, Furniture, Office Supplies) |
| **Sales** | The sales amount for each order |
| **Profit** | Profit derived from the order |
| **Quantity** | Quantity of items ordered |
| **Date** | The date the order was placed |
| **Region** | The region where the customer is located |

### Returns Table

| Column Name | Description |
|-------------|-------------|
| **Returned** | Indicates if the item was returned (Yes/No) |
| **Order ID** | Unique identifier for the order |
| **Market** | Region where the order was placed (e.g., LATAM, EU, APAC) |

### People Table

| Column Name | Description |
|-------------|-------------|
| **Person** | Name of the person or employee |
| **Region** | Region assigned to the person |

---

## Future Enhancements

### Potential Next Steps:
1. **Return Analysis**: Analyze the impact of returns on overall sales and profitability.
2. **Top Customers**: Identify top customers based on total order value or frequency.
3. **Segment Analysis**: Detailed analysis of customer segments (e.g., Consumer, Corporate, etc.).
4. **Market Analysis**: Deeper insights into geographical performance.
5. **Product Performance**: Evaluation of product-level performance to drive better product strategies.

---

## Conclusion

The **Dynamic Retail Dashboard** offers an insightful and dynamic view of the retail business's performance. It combines the power of Excel’s data transformation capabilities with interactive visualizations, enabling users to make data-driven decisions. The dashboard is designed for flexibility, allowing users to explore various aspects of the business through dynamic charts and KPIs. With future enhancements, the dashboard can be further expanded to answer additional business questions and support more detailed analyses.

---
