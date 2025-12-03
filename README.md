# Blinkit-Sales-Analysis-Dashboard
<img width="1345" height="727" alt="image" src="https://github.com/user-attachments/assets/a2fde59f-a8dc-47c6-8ed7-8f0bf44eb830" />

 ## Project Overview
This project presents a complete Business Intelligence solution for analyzing Blinkit’s sales, outlet performance, customer behavior, and product characteristics.
Using SQL for data cleaning and KPI calculations and Power BI for dashboard development, the analysis transforms raw retail data into meaningful insights that support business decision-making.

 ## Problem Statement
Blinkit requires a unified and reliable analytical framework to understand sales distribution across product categories, fat content types, outlet characteristics, and establishment years. The business needs clear visibility into customer preferences, revenue contribution patterns, outlet performance, and the relationship between product visibility, ratings, and sales.
A centralized BI dashboard is needed to support strategic planning, operational optimization, and data-driven decisions.
SQL · Power BI · Data Cleaning · KPI Engineering · Insight Storytelling

 ## Project Objectives

Clean and standardize the dataset using SQL

Prepare KPIs including:

Total Sales

Average Sales

Number of Items Sold

Average Rating

Develop seven business-required visuals

Build a  interactive Power BI dashboard

## Business Requirement Visuals

1️⃣ Total Sales by Fat Content

2️⃣ Total Sales by Item Type

3️⃣ Fat Content Contribution by Outlet Location

4️⃣ Sales Trend by Outlet Establishment Year

5️⃣ Sales Distribution by Outlet Size

6️⃣ Sales by Outlet Location Type

7️⃣ KPI Breakdown by Outlet Type (Matrix View)

## Tools Used

| Tool           | Purpose                                       |
| -------------- | --------------------------------------------- |
| **SQL Server** | Data cleaning, transformation, KPI generation |
| **Power BI**   | Dashboard creation & visualization            |
| **Excel**      | Data exploration                              |
| **DAX**        | Additional measures                           |


 ## Data Cleaning with SQL
 
 #### Standardizing Fat Content Labels
 UPDATE blinkit_data
SET Item_Fat_Content = 
    CASE 
        WHEN Item_Fat_Content IN ('LF', 'low fat') THEN 'Low Fat'
        WHEN Item_Fat_Content = 'reg' THEN 'Regular'
        ELSE Item_Fat_Content
    END;
    
#### KPI Queries
##### Total Sales

SELECT CAST(SUM(Total_Sales)/ 1000000 AS DECIMAL(10,2)) AS Total_Sales_Millons
FROM blinkit_data

##### Average Sales

SELECT CAST(AVG(Total_Sales) AS INT) AS Avg_Sales
FROM blinkit_data;


##### Number of Items Sold

SELECT COUNT(*) AS No_of_Items FROM blinkit_data;


##### Average Rating

SELECT CAST(AVG(Rating) AS DECIMAL(10,1)) AS Avg_Rating FROM blinkit_data;

## Key Insights
#### ⭐Product Insights

Fruits, Snacks, Frozen Foods, and Household items generate the highest revenue.

Seafood, Breakfast, and Hard Drinks are low-performing categories.

#### ⭐Customer Behavior

Low Fat products outperform Regular items in total sales contribution.

#### ⭐Outlet Characteristics

Medium-sized outlets contribute the highest revenue.

Tier 3 outlets outperform Tier 1 and Tier 2 outlets, indicating strong semi-urban demand.

#### ⭐Establishment Trends

Older outlets (established before 2005) consistently show high performance.

#### ⭐Ratings & Visibility

Average customer rating is 3.9, suggesting improvement opportunities.

Low visibility negatively impacts sales.

## Conclusion 
This project provides a comprehensive view of Blinkit’s sales and operational performance by combining SQL-based data preparation with a Power BI dashboard for business monitoring. The analysis highlights clear patterns in product demand, customer preferences, and outlet effectiveness across different sizes, locations, and establishment years. It also uncovers the impact of visibility and customer ratings on overall sales.

The final dashboard offers a structured and reliable reporting framework that enables informed decision-making in merchandising, outlet planning, and customer experience strategies. Overall, this project delivers a complete and actionable business intelligence solution tailored for retail sales analysis.

