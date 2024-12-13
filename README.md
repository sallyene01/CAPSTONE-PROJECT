# PROJECT TITLE; Sales Performance Analysis For a Retail Store
---
- [Project Overview](#project-overview)
- [Data Collected](#data-collected)
- [Project Objectives](#project-objectives)
- [KEY metrics](#key-metrics)
- [Tools Used](#tools-used)
- [Data cleaning and Preparation](##data-cleaning-and-preparetion)
- [Exploratory Data Analysis](##exporatory-data-analysis)
- [Visual Inference](##visual-inference)

## PROJECT OVERVIEW
----
This project collects and analyses sales performance Data from various regions.
The goal is to provide insights into sales of product over different region. The analysis focuses on understanding sales performance across regions and calculating key metrics such as average sales per product and total revenue by region. 


## DATA COLLECTED
---
The Data collected includes the following key columns;
- Region; The geographical location of each store
- Product; Items sold
- Order date; the day of the week for each transaction
- Quantity; The number of units sold for each transaction
- Unit Price; The amount for each product
- Revenue; The total monetary value generated from sale.
- Customer Name; Names of customers that patronzse the store
  

  ## PROJECT OBJECTIVES
  ---
  This project was designed to tackle the following analysis goal
  1. Sales per Product; To ascertain the total sales per product and the highest selling product
  2. Sales by Region; To determine the total sales by region
  3. Sales by Month; To work out overall sales for each month
  4. Average Revenue by Region; To calculate the avreage revenue per sales in each region.
  5. Transaction by Region; To figure out the number of units sold across different regions to be able to identify the most active location.
  6. Total Rvenue per product: To determine the product with the highest revenue
  7. Total Purchase Amount By Customer; To find the top 5 customers by the total purchase amount
  8. Percentage of Total Sales by Region; To calculate the percentage of total sales contributed by each region.
  9. Product By Order date; To identify products with no sales in the last quarter.
     
 
     ## KEY METRICS
     ---
     - Total sales; Sum of total sales categorized by
       1. Product
       2. Region
       3. Month
     - Units Sold; Sum of units sold grouped by region
     - Average Revenue; Total revenue for each region to evaluate revenue consistency.
     - Total Purchase by Customer; To check the top 5 customer.  
    

     ## TOOLS USED
     ---
     1. Microsoft Excel [DownloadHere](https://www.microsoft.com)
      - Summarize and format data for easier interpretation using pivot table.
      - Bar Charts were created to visually represent the key findings.
     2. SQL (structured query language) [DownloadHere](https://www.microsoft.com)
      - For querying data. Example:
        1. SELECT Product, SUM(UnitPrice) AS TotalSales
           FROM SalesData
           GROUP BY Product
        2. SELECT Region, COUNT(orderID) AS No_of_Transactions
           FROMSalesData
           GROUP BY Region
        3. SELECT Top (1) Product, SUM(UnitPrice)
           AS TotalSales
           FROM SalesData
           GROUP BY Product
           ORDER BY TotalSales DESC 
        4. SELECT Product, SUM(UnitPrice) AS TotalRevenue
           FROM SalesData
           GROUP BY Product  
        5. SELECT Month(orderDate) AS Month, SUM(UnitPrice) AS MonthlyTotal
           FROM SalesData
           WHERE YEAR(OrderDate) =2024
           GROUP BY Month(OderDate)
           ORDER BY Month
        6. SELECT Top (5) Customeer_id,
           SUM(UnitPrice) AS TotalPurchseAmount
           FROM SalesData
           GROUP BY Customer_id
           ORDER BY TotalPurchaseAmount DESC 
        7. SELECT Product FROM SalesData
           GROUP BY Product
           HAVING SUM(CASE WHEN OrderDate BETWEEN '2024-06-01' AND '2024-08-31' THEN 1 ELSE 0 END) = 0            
     3. Microsoft Power BI [DownloadHere](https://www.microsoft.com)
      - for data cleaning and fomatting
      - To visually represent the key findings
    

     ## DATA CLEANING AND PREPARATION
     ---
     The following actions were performed for the data cleaning and preparation
       1. Data loadind and inspection; Retrieve data from source and indentify missing or inconsistent values
       2. Data cleaning and Formatting; Identify and correct errors, inconsistencies and inaccuracies in the data, transform data into a consistent and suitable format for analysis.


          ## EXPLORATORY DATA ANALYSIS
          ---
          - Sales Per Product; Group data by product and sum of unit price column. This provides an overview of how much sales is realised from each product.
          - Sales by Region; Group data by region and sum of revenue column. To determine how much revenue each region is generating
          - Sales Per Month; Group data by month and sum of unit price column. To identify the period with the highest sales
          - Unit Sold by Region; Group data by region and sum of quantity column. To mearsure the most active region
          - Average Revenue by Region; To get the average revenue per transaction in each region.
         


            ## VISUAL ANALYSIS AND INFERENCE
            ---
            


<img width="160" alt="SALES BY REGION" src="https://github.com/user-attachments/assets/caf4e841-2b8d-4c3a-8981-f2d6a39d63f3">











<img width="170" alt="TOTAL SALES PER PPRODUCT" src="https://github.com/user-attachments/assets/566b232f-1a66-4343-a774-fb2b2bbac6de">













<img width="205" alt="TOTAL SALES PER MONTH" src="https://github.com/user-attachments/assets/c8d3cd1a-8e51-42bf-a776-6f9d8fa9f457">













<img width="182" alt="AVERAGE SALES PER PRODUCT" src="https://github.com/user-attachments/assets/52f8dbd5-1bdc-464d-8620-705137d50890">







<img width="137" alt="higest selling product" src="https://github.com/user-attachments/assets/76aed558-f4fe-4d3d-bd10-66b188dc1526">





<img width="230" alt="monthly sales total for current year" src="https://github.com/user-attachments/assets/ecbb1e9e-4d4f-479f-960b-aff085bec002">









<img width="301" alt="no of sales transaction by region" src="https://github.com/user-attachments/assets/4e17c9be-6902-4583-961c-fd53c1a2855b">








<img width="196" alt="products with no sales in the last quarter" src="https://github.com/user-attachments/assets/cc841f83-3935-441b-9e0a-8f0989cf1f90">









<img width="256" alt="TOP 5 CUSTOMERS" src="https://github.com/user-attachments/assets/70c2aaa6-3fe3-429e-bf7b-dd12a093ae6c">











<img width="247" alt="total revenue per product" src="https://github.com/user-attachments/assets/faf70f62-81d2-471d-9263-29c07043914f">









<img width="259" alt="total sales for each product" src="https://github.com/user-attachments/assets/f9bc5821-9f61-4d73-a6a9-687c14a05150">














![POWER BI S,CD](https://github.com/user-attachments/assets/f8077b97-a109-4cfb-9895-9ed17491a229)
















<img width="209" alt="AVERAGE BY REGION" src="https://github.com/user-attachments/assets/b096ed62-394e-4ae0-9846-6ec03fd4cd6b">








