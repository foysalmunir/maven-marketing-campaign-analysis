# 📊 Maven Marketing: Customer & Campaign Analytics

## Executive Summary
This project is an end-to-end data analytics solution designed to evaluate the performance of marketing campaigns and uncover the "ideal customer persona" for a global retail company. By processing over 2,200 customer records, I developed an interactive Power BI dashboard that provides actionable insights into demographic behavior, product category performance, and channel conversion rates.

**Tools Used:** Excel (Data Cleaning), Power Query (Data Transformation), Power BI & DAX (Modeling & Visualization).

---

## 🎯 The Business Problem
The Maven Marketing team needed data-driven answers to the following questions to optimize their future marketing budget:
1. What does the "average customer" look like?
2. Which product categories drive the most revenue?
3. Are there inefficiencies in our purchasing channels (Web vs. Store)?
4. Which marketing campaigns delivered the highest ROI?

---

## 🛠️ Data Processing & Methodology

Raw data is rarely perfect. Before visualizing the data, I performed rigorous data pre-processing to ensure statistical accuracy:

* **Handling Missing Data:** Identified missing values in the `Income` column. Rather than deleting these records, I performed **Median Imputation stratified by Education level** to preserve the dataset's integrity without skewing income distributions.
* **Outlier Removal:** Filtered out erroneous data entry points, including severe birth year anomalies (e.g., records dating back to 1893) and extreme income outliers (max $666,666).
* **Feature Engineering (Power Query):** Created net-new calculated columns to enable deeper analysis, including `Customer Age`, `Total Spending`, and `Total Childrens`. 
* **Data Binning:** Grouped continuous variables (like `Web Visits per Month`) into discrete categorical bins (0-3, 4-6, 7-8, 9+) to accurately map engagement vs. conversion trends.

---

## 💡 Key Business Insights

### 1. The Core Customer Persona
The primary revenue driver for Maven Marketing is "Middle-Aged Graduates." The average customer is a **55-year-old married graduate** with a household income of **~$51.6K** and one dependent. 

### 2. The Product Revenue Mix
Out of the $1.35 Million in total revenue analyzed, **Wines ($680K)** and **Meat Products ($368K)** account for nearly 80% of all sales. Sweets and Fruits are heavily underperforming and may require bundling strategies.

### 3. The "Window Shopper" Web Paradox
A correlation analysis between Web Visits and Web Purchases revealed a surprising inefficiency:
* Customers who visit the site moderately (**4–6 times/month**) have the highest purchase conversion rate.
* Customers with the highest engagement (**9+ visits/month**) actually buy *less* on average. This indicates high-frequency visitors are likely hunting for discounts or struggling with website UX, representing a massive retargeting opportunity.

### 4. Campaign Success Rate
By switching the aggregation model from binary counts to absolute sums, the data revealed that the **Final "Response" Campaigns** were overwhelmingly the most successful (~334 acceptances), outperforming Campaign 2 by over 1,000%.

---

## 🖥️ Dashboard Preview

Maven Marketing Power BI Dashboard

<img width="1167" height="660" alt="image" src="https://github.com/user-attachments/assets/fa4db951-8bdf-4df4-aa38-fc5818fba4b4" />


*(Note: Click the image above to view the full resolution, or download the `.pbix` file to interact with the dashboard directly.)*

---

## 📂 Repository Structure
* `/data/` - Contains the raw data dictionary and the cleaned CSV dataset.
* `/dashboard/` - Contains the final Power BI (`.pbix`) file.
* `/images/` - High-resolution screenshots of the visualizations.

## 🚀 How to Interact with this Project
1. Clone this repository.
2. Open the `Marketing Campaign Results.pbix` file using Power BI Desktop.
3. Use the Tile Slicers at the top of the dashboard to filter the data dynamically by Country to see regional differences in buying behavior.
