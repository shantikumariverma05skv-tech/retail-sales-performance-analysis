# Retail Sales Performance Analysis & Business Insights (Python)

![Python](https://img.shields.io/badge/python-3.10-blue)
![Status](https://img.shields.io/badge/status-completed-brightgreen)

Analyzing retail sales transaction data to extract actionable business insights on revenue performance, customer behavior, and regional demand.

## Table of Contents

- [Objective](#objective)
- [Tools & Libraries](#tools--libraries)
- [Dataset](#dataset)
- [Data Cleaning & Preprocessing](#data-cleaning--preprocessing)
- [KPI Overview](#kpi-overview)
- [Insights & Visualizations](#insights--visualizations)
  - [Top 10 Customers](#top-10-customers)
  - [Top 10 Products by Sales](#top-10-products-by-sales)
  - [Sales by Region](#sales-by-region)
  - [Monthly Sales Trends](#monthly-sales-trends)
- [Data Challenges & Mitigations](#data-challenges--mitigations)
- [Key Learnings](#key-learnings)
- [Skills Demonstrated](#skills-demonstrated)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [Author & Contact](#author--contact)


## Objective

To analyze retail sales transaction data and provide actionable insights on revenue performance, customer concentration, and regional demand to support data-driven business decisions.

## Tools & Libraries

- **Python** for data analysis
- **Pandas** for data manipulation
- **NumPy** for numerical operations
- **Matplotlib** for data visualization

## Dataset

- **Overview:** Simulated retail transaction dataset representing real-world sales operations.
- **Contents:** Order-level data including product, customer, region, date, and sales value.
- **Source:** [Superstore Sales Dataset retrieved from Kaggle](https://www.kaggle.com/datasets)

### Dataset Preview


| Order ID         | Customer Name     | Product          | Region | Order Date | Sales    |
|-----------------|-----------------|-----------------|--------|------------|---------|
| CA-2017-152156  | Claire Gute      | Furniture       | South  | 2017-11-11 | 261.96  |
| CA-2017-138688  | Darrin Van Huff  | Office Supplies | West   | 2017-06-16 | 14.62   |


## Data Cleaning & Preprocessing

- Removed duplicate transaction records
- Handled missing sales and customer values
- Standardized date formats for time-series analysis
- Corrected inconsistent column naming

**Insights:**  
Records with missing sales values were excluded to avoid inaccurate revenue calculations.
- All other columns have 0 missing values → dataset is clean.
- Data is ready for further analysis (KPIs, customer/product analysis).
  
## KPI Overview

- **Total Revenue:** 2.26M
- **Total Orders:** 4,922
- **Total Customers:** 793
- **Average Order Value:** 459.48

These KPIs establish a baseline for evaluating customer purchasing behavior and revenue distribution.

## Insights & Visualizations

### Top 10 Customers


<img width="643" height="449" alt="03_Top_Customers2" src="https://github.com/user-attachments/assets/32cede25-1cfd-471b-aae9-fd541bedaaed" />


**Contribution:**
**6.8%** of total revenue

**Insight:**
Low customer concentration risk; revenue is distributed across a broad customer base.

**Business Recommendations:**
- Implement loyalty programs to retain high-value customers
- Expand acquisition strategies to reduce over-dependence on a few customers

### Top 10 Products by Sales


<img width="512" height="500" alt="04_Top_Products4" src="https://github.com/user-attachments/assets/03c12d69-4f7e-4380-bb23-522eb86ef024" />


 **Insight:**
 The top 10 products contribute **10.82%** of total revenue, indicating a diversified product portfolio with no excessive dependency on a small set of products. 
 
 **Business Recommendation:**
- Strengthen inventory planning for top products
- Diversify promotions to mid-tier products to reduce dependency risk These products can be prioritized for demand forecasting and inventory planning.

### Sales by Region


<img width="533" height="326" alt="05_Region_Sales" src="https://github.com/user-attachments/assets/aba7d083-18ec-41a5-846a-3a8a4a3f31c5" />


**Insight:**
The South region underperforms compared to East and West, indicating potential pricing, demand, or distribution inefficiencies compared to higher-performing regions.

**Business Recommendation:**
- Prioritize marketing spend and stock availability in West
- Investigate low-performing regions for pricing or logistics issues

### Monthly Sales Trends


<img width="769" height="434" alt="06_Monthly_Trend2" src="https://github.com/user-attachments/assets/15c18037-989b-42e2-b1c7-1062b613128f" />


**Insight:**
Monthly sales trends reveal fluctuations in demand across periods, with both positive and negative month-over-month growth, highlighting the presence of seasonality and varying customer demand. This analysis supports proactive inventory and promotional planning.

**Business Recommendation:**
- Align inventory and staffing with peak months
- Run targeted promotions during low-sales periods to stabilize revenue
  
## Data Challenges & Mitigations

- **Missing Values:** Handled missing sales values by excluding records
- **Inconsistent Formats:** Standardized date formats for consistent time-series analysis
- **Duplicate Records:** Removed duplicates to ensure accurate KPI calculation

## Key Learnings

- Data cleaning and preprocessing for messy transactional data
- KPI calculation and business insight generation
- Data visualization for decision-making support
- Understanding customer concentration, revenue distribution, and regional performance
- Translating raw data into actionable business strategies

## Skills Demonstrated

- Python Programming
- Data Analysis with Pandas & NumPy
- Data Visualization with Matplotlib
- KPI computation & business insights
- Problem-solving with real-world business datasets

## Conclusion

This project demonstrates my ability to transform raw transactional data into business-ready insights to support decisions in:

- Sales strategy optimization
- Regional planning
- Customer management

## Project Structure

Retail_Sales_Analysis/
│
├── Retail_Sales_Analysis.ipynb
├── data/
│ └── retail_dataset.csv
├── images/
│ ├── top_customers.png
│ ├── top_products.png
│ └── sales_by_region.png
└── README.md

## How to Run

1. Clone this repository
2. Install required libraries: `pip install pandas numpy matplotlib`
3. Run `Retail_Sales_Analysis.ipynb` in Jupyter Notebook
4. Explore outputs and visualizations

## Author & Contact

**Author:** Shanti Kumari Verma  
**GitHub:** [https://github.com/shantikumariverma05skv-tech](https://github.com/shantikumariverma05skv-tech)  
**LinkedIn:** [https://www.linkedin.com/in/shantikumariverma05skv-tech](https://www.linkedin.com/in/shantikumariverma05skv-tech)  
**Role Simulated:** Data Analyst / Business Analyst
