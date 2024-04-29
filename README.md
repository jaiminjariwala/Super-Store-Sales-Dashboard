# SuperStore Sales PowerBI Dashboard

# `Project Objective:`
## To develop a comprehensive Super Store Sales PowerBI dashboard that provides real time insights into key-performance-metrics and trends.

# `Preparing Data:`
1. Prepare/Download the given CSV files
2. Load File (from Get Data) into PowerBI and perform necessary Transformations on columns if required.
<img width="551" alt="image" src="https://github.com/jaiminjariwala/Super-Store-Sales-Dashboard/assets/157014747/0fdd2589-915a-4d88-80df-33224cf23414">


# `DAX Queries Written:`
1. Created (Order and Shipping Date Days Duration) column
   ```
   Difference between Order Date and Shipping Date = DATEDIFF('Sheet1'[Order Date], 'Sheet1'[Ship Date], DAY)
   ```
   
2. Created (SalesForeCast) NEW TABLE in order to get (SUM OF SALES) by performing (GROUP BY ON ORDER_DATE COLUMN), with intention to get sum of sales done from different customerID on that particular date.
   ```
   SalesForeCast = SUMMARIZE('Sheet1', 'Sheet1'[Order Date], "Total Sales", SUM(Sheet1[Sales]))
   ```
