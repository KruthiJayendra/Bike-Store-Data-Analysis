# Bike-Store-Data-Analysis

## OBJECTIVE 🎯
To understand the inventory and analyse the Sales of the different branches of bike store as well as the employee performance.
## PROBLEM STATEMENT
The objective of this data analysis is to comprehensively understand and evaluate the inventory management, sales performance, and employee efficiency across various branches of a bike store chain. By conducting a thorough examination of inventory levels, sales data, and employee performance metrics, the analysis aims to identify key factors that influence sales outcomes, optimize inventory distribution, and enhance employee productivity. This will enable the bike store to make data-driven decisions to improve overall operational efficiency, increase sales, and enhance customer satisfaction across all branches. 

## DATASET
Available in the repository
### ENTITY RELATIONSHIP DIAGRAM OF THE DATASET
![Bike-store-ERD](https://github.com/KruthiJayendra/Bike-Store-Data-Analysis/assets/113492040/30c1ae68-b3ad-42ea-a7ae-5a3488f7dafe)

## TECHNOLOGY
Business Intellegence
## TOOLS
Python, SQL, MS Excel
Libraries Used: numpy, pandas, sqlite3, matplotlib ,datetime

## INTRODUCTION
Bike Store Relational Database is the sample database from sqlservertutorial.net.
The dataset contains 9 tables in total
1. Production: Feild Definitions
   * Categories - category_id **(Primary Key)** , category_name (Name of the categories of the Bikes available in the stores) - 7 Rows x 2 Columns
   * Products - product_id **(Primary Key)**, product_name, brand_id, category_id, model_year, list_price - 321 Rows x 6 Columns
   * Stocks - (store_id, product_id) **(Primary Key)**, quantity - 939 Rows x 3 Columns
   * Brands -brand_id **(Primary Key)** , brand_name - 9 Rows x 2 Columns
3. Sales:
   * Customers - customer_id  **(Primary Key)** , staff_id, first_name, last_name,phone, email, street, city, state, zipcode - 1445 Rows x 9 Columns
   * Orders - order_id  **(Primary Key)** , customer_id , order_status , order_date , required_date , shipped_date, store_id, staff_id - 1615 Rows x 8 Columns
   * Staff - staff_id  **(Primary Key)** , first_name, last_name, email, phone, active, store_id, manager_id - 10 Rows x 8 Columns
   * Order_items - (order_id, item_id)  **(Primary Key)** , product_id, quantity, list_price, discount - 4722 Rows x 6 Columns
   * Stores - store_id  **(Primary Key)** , store_name, phone, email, street, city, state, zipcode - 3 Rows x 8 Columns
   
The attached  code performs data extraction, transformation, loading (ETL), and analysis on a dataset of a bike store. The dataset is first loaded from CSV files into pandas DataFrames, then transferred into a SQLite database. Various SQL queries are executed on the database to retrieve insights, and the results are visualized using matplotlib.

## QUESTIONS
1. What is the number of stocks based on category name and store name?
2. Number of order items based on category name and store name?
3. What are the Total sales in Santa Cruz Bikes based on year month?
4. What are the Total sales in Baldwin Bikes based on year month?
5. What are the Total sales in Rowlett Bikes based on year month
6. Which Staff has the highest number of orders?
7. Which Staff has the lowest number of orders?

# PROCESS
The attached  code performs data extraction, transformation, loading (ETL), and analysis on a dataset of a bike store. The dataset is first loaded from CSV files into pandas DataFrames, then transferred into a SQLite database. Various SQL queries are executed on the database to retrieve insights, and the results are visualized using matplotlib.
 
 
 
 # QUERYS




1. Import Libraries
The necessary libraries for data manipulation, database operations, and visualization are imported.

2. Read Data from CSV Files
The data is read from CSV files into pandas DataFrames, covering brands, categories, customers, order items, orders, products, staffs, stocks, and stores.

3. Connect to SQLite Database
A connection to a SQLite database is established.

4. Load DataFrames into SQLite Database
Each DataFrame is loaded into the SQLite database, replacing any existing data.

5. Run SQL Queries and Load Results into DataFrames
SQL queries are executed to retrieve data, which is then stored in pandas DataFrames.

 
# Analysis and Visualization
## Question 1
**Number of Stocks Based on Category and Store**

**SQL Query:** Joins the categories, products, stocks, and stores tables to aggregate the total stock quantity by category and store.

**Data Transformation:** Converts store and category names to categorical data.

**Visualization:** Bar chart showing stocks per category for each store.
**From the Analysis it is observed that Cruisers Bicycles has the highest amount of Inventory with	1148,1137,1093 number of bikes across all 3 stores and Cyclocross Bicycles	has the lowest inventory with 97, 159, 158 number of bikes; An assumption can be made that Cyclocross Bicycles are the fastest moving an selling products out of all the categories and hence can be produced rapidly to balamce the stocks, where as production on Cruisers Bicycles maybe slowed down.**
![image](https://github.com/KruthiJayendra/Bike-Store-Data-Analysis/assets/113492040/6f7d7bf5-7e9c-4c9f-b574-39cc24ac36ba)


## Question 2
**Number of ordered items based on category name and store name**
**SQL Query:**  Joins the categories, products, order_items, orders, and stores tables to aggregate the total order quantity by category and store.

**Data Transformation:** Converts store and category names into categorical data types to maintain the order.

**Visualization:** Bar chart showing order items per category for each store.
From the Analysis it is observed that 
1. Best Performing Store: Baldwin Bikes (4779 ordered items)
2. Medium Range Performing Store: Santa Cruz Bikes (1516 ordered items)
3. Performing Store: Rowlett Bikes (783 ordered items)

Baldwin Bikes: Expand inventory and target marketing to maintain and boost performance.
Santa Cruz Bikes: Increase marketing efforts and gather customer feedback for improvement.
Rowlett Bikes: Analyze market, promote products effectively, and improve customer experience.
   

![image](https://github.com/KruthiJayendra/Bike-Store-Data-Analysis/assets/113492040/24ed9c3a-174f-46b5-b0f0-41bb2ccafaf4)


## Question 3
**Total Sales in Santa Cruz Bikes by Year-Month**
**SQL Query:**  Joins the order_items, orders, and stores tables, and filters by store name ('Santa Cruz Bikes'). Aggregates the total sales for each year and month.
**Data Transformation:** Converts the year-month string into a datetime object for plotting.

**Visualization:** Line chart showing monthly sales over time.
Peak Performance: The highest sales were in April 2018, which indicates a seasonal spike or a successful promotional campaign; Sales in  437,264.91 in USD.
Dramatic Drop: There is a significant drop in sales towards the end of 2018, with the lowest in November 2018; Sales in 5,257.97 in USD.
By understanding the highest and lowest sales months, Santa Cruz Bikes can better strategize their marketing, inventory, and customer engagement efforts to maintain consistent sales throughout the year and avoid periods of low performance.
![image](https://github.com/KruthiJayendra/Bike-Store-Data-Analysis/assets/113492040/05ad4953-5098-4ef1-bf6c-6b7db773aeea)


## Question 4
**Total Sales in Baldwin Bikes Bikes by Year-Month**
**SQL Query:** Joins the order_items, orders, and stores tables, and filters by store name ('Baldwin Bikes'). Aggregates the total sales for each year and month.

**Data Transformation:** Converts the year-month string into a datetime object for plotting.

**Visualization:** Line chart showing monthly sales over time.
Peak Performance: The highest sales were in April 2018, indicating a seasonal peak or a successful promotional campaign; Sales in 437,264.91 in USD
Significant Drop: There is a significant drop in sales in June 2018, which might be due to seasonal factors, market conditions, or internal issues; Sales in 188.99 in USD.
Investigate the factors contributing to the peak sales in April 2018. Replicate successful marketing campaigns or promotions that led to high sales during this period. Examine the reasons behind the low sales in June 2018. Identify any external or internal factors, such as market conditions, competition, or operational issues, and take corrective actions.
![image](https://github.com/KruthiJayendra/Bike-Store-Data-Analysis/assets/113492040/a32a0803-4dbc-4e0c-bb0f-10d852d76233)


## Question 5
**Total Sales in Rowlett Bikes by Year-Month**
**SQL Query:** Joins the order_items, orders, and stores tables, and filters by store name ('Rowlett Bikes'). Aggregates the total sales for each year and month.

**Data Transformation:** Converts the year-month string into a datetime object for plotting.

**Visualization:** Line chart showing monthly sales over time.
Peak Performance: The highest sales were in April 2018, indicating a seasonal peak or a successful promotional campaign; Sales is 75,609.27 in USD
Significant Drop: There is a significant drop in sales in July 2017, which might be due to seasonal factors, market conditions or internal issues;Sales in 1,618.15.
Implement promotional strategies around peak sales months to capitalize on potential high demand. Use targeted promotions during historically low sales months to boost customer engagement and sales.
![image](https://github.com/KruthiJayendra/Bike-Store-Data-Analysis/assets/113492040/1f5ac6b0-f72d-450d-a488-d6deff34e11b)


## Question 6
**Staff with highest number of orders**

**SQL Query:** Joins the orders and staffs tables to count the number of orders handled by each staff member. Identifies the staff member with the highest number of orders.

**Result:** The DataFrame shows the staff ID, first name, last name, and the number of orders for the staff member with the highest order count.
### The staff with Staff-ID 6 Name	Marcelene	Boyer	has the highest number of orders i.e 553

## Question 7
**Staff with lowest number of orders**

**SQL Query:** Joins the orders and staffs tables to count the number of orders handled by each staff member. Identifies the staff member with the lowest number of orders.

**Result:** The DataFrame shows the staff ID, first name, last name, and the number of orders for the staff member with the lowest order count.
### The staff with Staff-ID 9 Name	Layla	Terrell	has the lowest number of orders i.e 86

# Summary
This code reads bike store data from CSV files, loads it into a SQLite database, runs queries to gather insights, and visualizes the results. It uses pandas for data manipulation, SQLite for database operations, and matplotlib for visualization.
