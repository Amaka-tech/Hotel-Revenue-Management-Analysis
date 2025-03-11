# Hotel-Revenue-Management-Analysis
As a hypothetical BI Insights Manager,  my job is to create a deep-dive analysis report in Power BI about the Hotel Revenue Management of a fictional company named "Yusen logistics".

---

![](Yusen_Logistics.png)

---
## Introduction:

The Yusen Hotel Management analysis was prepared with Microsoft Excel and PowerBI. Time analysis exploration into reservation trends was performed including Seasonality, Festive periods, weekday vs weekend etc. Key insights into the performance of several Agents and overall hotel performance from set KPI were gained. Further insights on Customers type (family with children, single or couples visitors) were also obtained.

---
## Problem Statement:

The objectives of the analysis are:
- Perform Time analysis exploration into reservation trends.
- identify the top performing agents.
- use KPIs to measure the performance of the hotels with respect to the revenue generated.
- use the insights gained to make recommendations for optimization.

---
## Data Source:

The datasets used for this project was from a Microsoft Excel workbook provided by the Tech Instistute "DAHEL Techies" where I completed my internship. I studied the datasets alongside the data dictionary and figured out the approach to take for the analysis. 

Click [here](Dataset.xlsx) for Datasets. Also refer to [data dictionary](Dataset_dictionary.xlsx)

---
## Data Transformation:

1. Imported Excel workbook into Power Query Editor using the "Get Data" feature
2. Used Power Query Editor to clean and transform data as follows:
   - Promote headers
   - Append and Merge datasets from three separate tables to form one table
   - Create new columns, delete columns, reorder columns, merge columns
   - Change data type for each column to correspond with the values
   - Replace "null" values
   - Filter rows
   - Use Column quality, Column distribution and/or Column profile to verify that data is 100% clean.
   - Import cleaned data from Power Query Editor into PowerBI desktop
3. Create measures in PowerBI to calculate hotel cancellation rate, total revenue, total loyal customers, etc for Data visualization.
4. Create key performance indicators (KPIs) and other business calculations,
5. Carry out DAX calculations for solving statistical measures and other mathematical formulas.
6. Data Modelling
7. Data Visualization using various tools:
   - Navigation panes
   - Cards, Clustered column chart, KPI, Slicer, Line chart, Donut chart, pie chart, Area chart, clustered bar chart
   - Filter
   - Text box

Please Note: I have attached the file for my completed [PowerBI project](Power BI Project - Okonkwo Chiamaka I..pbix) for reference

---
## Data Modelling:

The intelligence in PowerBI makes it such that tables are automatically joined by creating relationships with them. However, as someone who understands the dataset and wants to get specific insights and information. I had to create other relationships and measures to enable me. so I did another model. I created 7 dimension tables and 2 fact tables as I hoped for a Star Schema.

![]()

---
## Data Analysis:

Several expressions and functions were made to arrive at the desired KPI or Metrics. I would list a few:

Cost of Goods Sold = SUM( 'Production Product_view'[StandardCost]) * SUM('Sales SalesOrderDetail_view'[OrderQty])
CycleTime = SUM( 'Production WorkOrderRouting_view'[ActualResourceHrs] ) / SUM ( 'Production WorkOrder_view'[OrderQty])
OnTimeProductionPercent = VAR Num_0 = COUNTROWS(FILTER('Production WorkOrderRouting_view', 'Production WorkOrderRouting_view'[OnTime] = 0)) VAR Num_1 = COUNTROWS(FILTER('Production WorkOrderRouting_view', 'Production WorkOrderRouting_view'[OnTime] = 1)) RETURN Num_1/(Num_0+Num_1)
Stock Turn = [COGS]/[CostofInventory]
ABC Ranking and XYZ analysis was also done.
All the formlulas for the calculated columns and measures can not be well explained by just writing the expressions here as they are written on various tables. Kindly pardon me 😄

---
## Data Visualization

The dashboards are divided into two major sections:
1.	Hotel Reservation Analysis
2.	Revenue Analysis

The report consists of 4 pages

The Inventory Page
The Product Page
The Sales Page
insight Page
The report can be interacted with on the PowerBI service here:

---
## Features of the Report
The hamburger icon is a button that helps you to view the different pages. When you hover on it, you will see an effect and a click on it will open up a navigation pane that has buttons to direct you to the desired page you want to see. After which you can always return to the hamburger button when done. To get the insight, you click on the black info icon which will lead you to the insight page. The LinkedIn icon functions very well too as a click on it will take you to my LinkedIn profile if you wish to contact me. I think you should. so i know how you feel about this project 😀

Here are the reports:

Inventory Page

![]()

Product Page

![]()

Sales Page

![]()

Insight Page

![]()

---
## Analysis

The Company has 14 location for production/storage
There are 4 main categories of products (Bikes, Accessories, Clothing and Components)
The value of goods in the warehouse is about 74 billion USD
Bike sales has the highest impact on Inventory and Sales followed by Accessories.
There is a 42% Stock turn ratio
On time Production is 48%
93% of the entire products needs to be replaced for sales.

---
## Insights and Recommendation





