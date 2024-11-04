## LITA-Project-2

### PROJECT TITLE: SALES ANALYSIS

[PROJECT OVERVIEW](project-overview)

[DATA SOURCE](data-source)

[TOOLS USED](tools-used)

[DATA PREPARATION AND CLEANING](data-preparation-and-cleaning)

[EXPLORATORY DATA ANALYSIS](exploratory-data-analysis)

[DATA ANALYSIS](data-analysis)

[DATA VISUALIZATION](data-visualization)

### PROJECT OVERVIEW
This project shows the performnace of each product sold. It takes into consideration the revenue derived from various regions on each product over the years breaking it down into quarters,it indicates how the quantity sold changes overtime and it also looked into the region and product with the highest revenue. 

### DATA SOURCE
The source of the data is an assignment that was given to us by Incubator Hub to test our level of understanding based on the classes we did over the last 3 months.
- Columns in the data
    * OrderID
    * Customer Id
    * Product
    * Region
    * Quantity
    * UnitPrice($)
    * Sales($)

### TOOLS USED
- Microsoft Excel
- Power BI(Power Query)
- Microsoft Power BI
- SQL Server

### DATA PREPARATION AND CLEANING
- Microsoft Excel
    * For Data loading and preparation: Here, I Used CTRL+A to select the entire table,ALT+H+O+I to autofit the columns which could also be done by writing some lines of code and also ALT+A+M to remove duplicates.I did all this before exporting my data to Power BI for cleaning.

 - Power BI(Power Query)
     * For Data Cleaning : Power BI already fixed the data type for me, then I went on to insert a custom column to multiply the unit price with the quantity sold to get the revenue derived from each product each day,I had to duplicate the "OrderDate" column to split the date into years, months, and days.
       I moved to the canvas to build my dashboard.
       
- Just before I built my dashboard I exported my data to SQL Server for data quering,where I was trying to derive the total revenue from each region and each products
         
- Microsoft Power BI
     * For Visualization
 
### EXPLORATORY DATA ANALYSIS
- What is the total revenue derived from each products ?
- What is the total quantity sold in each region ?
- Sum of sales in each quarter of the year

### DATA ANALYSIS
```
SELECT Product, SUM(Sales) Total_Sales
FROM [dbo].[LITA Capstone Dataset (WORK1)]
GROUP BY Product
ORDER BY SUM(Sales) DESC
```
![Untitled 2](https://github.com/user-attachments/assets/169ee4bc-0a2d-458a-a392-08b40623463a)

### DATA VISUALIZATION 
![Sales Analysis (Real)_page-0001 (1)](https://github.com/user-attachments/assets/d9cc4551-7aa4-4dc8-b272-588fa35375c3)

### CONCLUSION 
This analysis shows that the business made the highest sales in February with a revenue of $546,300 in the month of Febraury.The highest sales was made from the East and the best performing product is "Shoe"
The data is not comprehensive enough in that it doesn't reveal the profit made from the sales made in each region and on different products as a result of that we cannot make a decison on whether the business is performing well or not
