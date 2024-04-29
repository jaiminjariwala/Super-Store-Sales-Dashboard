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

# `TOP 5 Project Insights:`
1. Top 5 States which led to generate more sales are California, NY, Texas, Washington and Pennsylvania as seen below <br>
   > EASTERN Zone States have contributed ($450K / $2M) which is `22.8%` of total Sales generated. 
   <img width="281" alt="image" src="https://github.com/jaiminjariwala/Super-Store-Sales-Dashboard/assets/157014747/76bbf816-58f4-46b5-b31a-2e5776b98a35">
   <img width="305" alt="image" src="https://github.com/jaiminjariwala/Super-Store-Sales-Dashboard/assets/157014747/68d535b2-a328-44a4-aae7-2878c6231908">

2. `Customers preferred Cash-On-Delivery (COD) as their payment mode` more, following Online and Cards! <br><br>
   <img width="200" alt="image" src="https://github.com/jaiminjariwala/Super-Store-Sales-Dashboard/assets/157014747/b6a3531a-187e-4ccb-8786-c1ff2bd6d667">

3. Sales and Profit's Rises from August to December month
   > Though Sales Increased but Profit🔻Decreased in month of November
   <img width="620" alt="image" src="https://github.com/jaiminjariwala/Super-Store-Sales-Dashboard/assets/157014747/a1d04ad0-c44b-4f00-ae2f-0f84a783ee40">

4. We can `Expect an Average Sum of Sales from beginning of next year as $5.2K` <br><br>
   <img width="590" alt="image" src="https://github.com/jaiminjariwala/Super-Store-Sales-Dashboard/assets/157014747/85a3e306-b411-483d-8e3a-7035fdd350d4">

5. `Customers mostly preferred Standard Class which delivers Products in 5-7 days` following Second, First Class and Same Day Delivery!
   > Standard Class Delivery Customers contributes ( $912K / $2M ) `45.6%` of Total Sales
   <img width="221" alt="image" src="https://github.com/jaiminjariwala/Super-Store-Sales-Dashboard/assets/157014747/d193ba08-685b-4d32-80b4-b424f25baeec">

