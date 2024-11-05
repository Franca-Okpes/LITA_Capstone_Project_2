# LITA_Capstone_Project_2

## Project Title: Customer Segmentation for a Subscription Service 

[Project Overview](#project-overview)


[Data Sources](#data-sources)


[Tools Used](#tools-used)


[Data Cleaning and Preparations](#data-cleaning-and-preparations)


[Exploratory Data Analysis (EDA)](exploratory-data-analysis-eda)


[Data Analysis](#data-analysis)


[Data Visualization](#data-visualization)

- Project Overview
This project analyzes customer data for a subscription service to uncover behavioral patterns, segment types, and key trends in subscription cancellations and renewals. The final deliverable is a Power BI dashboard that visualizes insights, enabling data-driven decisions to improve customer retention and subscription offerings.

- Data Sources
The primary source of Data used here is a DataSale.xlsx which is an open source Data that can be freely downleaded from an open source online such as Kaggleor FRED or any other Data repository site.

-Tools Used
The tools used in analysing the Dataset from the retail shop are

- Microsoft Excel [Download Here](https://www.microsoft.com)

 1. For Data cleaning
 2. For Analysis
 3. For Data Visualization


 - SQL Structure Query ([Download Here](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
   SQL Server Management Studio (SSMS) - Tool to Manage SQL Server:[Download Here](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms)
 
   SQL Structure Query Language for Quering Data

- Power Bi [Download Here](https://powerbi.microsoft.com/desktop/)

   Power Bi for visualization of the analysis carried out on Microsoft Excel and SQL

- Github for Portfolio Building

### Data Cleaning and Preparations

In the initial phase of Data cleaning and preparation, I performed the following action;
1.Data Importation and Inspection
2.Handling missing variables
3.Data Cleaning and Formatting

- Exploratory Data Analysis (EDA)
  Exploratory Data Analysis (EDA) helps uncover insights by addressing key questions such as:

1.What is the average duration of subscriptions?
2.Which subscription type is the most popular?
3.Which customers have canceled their subscriptions?
4.What is the total revenue for each subscription type?
5.Which are the top three regions with the highest subscription cancellations?

Data Analysis
This is the section I included my basic lines of code or queries or even some of the DAX (Data Analysis Expression) ecpressions used during the analysis;

Eg

```SQL
SELECT region, COUNT(customerid) AS total_customers
FROM [dbo].[LITA Capstone CustomerDatabase]
GROUP BY region;
```

```SQL
SELECT TOP 1 
    subscriptiontype, 
    COUNT(customerid) AS total_customers
FROM [dbo].[LITA Capstone CustomerDatabase]
GROUP BY 
    subscriptiontype
ORDER BY 
    total_customers DESC;
```

```SQL

SELECT customerid, canceled
FROM [dbo].[LITA Capstone CustomerDatabase]
WHERE canceled =1 
```

```SQL
select top 3
region,
 COUNT(customerid) AS cancellations
FROM [dbo].[LITA Capstone CustomerDatabase]
WHERE canceled IS NOT NULL
GROUP BY region 
ORDER BY cancellations DESC;
```


Data Visualization
