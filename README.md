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
   * Categories - category_id **(Primary Key)** , category_name (Name of the categories of the Bikes available in the stores)
   * Products - product_id **(Primary Key)**, product_name, brand_id, category_id, model_year, list_price
   * Stocks - (store_id, product_id) **(Primary Key)**, quantity
   * Brands -brand_id **(Primary Key)** , brand_name 
3. Sales:
   * Customers - customer_id  **(Primary Key)** , staff_id, first_name, last_name,phone, email, street, city, state, zipcode
   * Orders - order_id  **(Primary Key)** , customer_id , order_status , order_date , required_date , shipped_date, store_id, staff_id
   * Staff - staff_id  **(Primary Key)** , first_name, last_name, email, phone, active, store_id, manager_id
   * Order_items - (order_id, item_id)  **(Primary Key)** , product_id, quantity, list_price, discount
   * Stores - store_id  **(Primary Key)** , store_name, phone, email, street, city, state, zipcode
   
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

SQL Query: Aggregates total stock quantity by category and store.

Data Transformation: Converts store and category names to categorical data.
Visualization: Bar chart showing stocks per category for each store.
Number of Order Items Based on Category and Store

## Question 2
**Number of ordered items based on category name and store name**
SQL Query: Aggregates total stock quantity by category and store.

Data Transformation: Converts store and category names to categorical data.

Visualization: Bar chart showing order items per category for each store.

## Question 3
**Total Sales in Santa Cruz Bikes by Year-Month**
SQL Query: Aggregates total sales by year and month for 'Santa Cruz Bikes'.

Data Transformation: Converts year-month to datetime.

Visualization: Line chart showing monthly sales over time.

## Question 4
**Total Sales in Baldwin Bikes Bikes by Year-Month**
SQL Query: Aggregates total sales by year and month for 'Baldwin Bikes'.

Data Transformation: Converts year-month to datetime.

Visualization: Line chart showing monthly sales over time.

## Question 5
**Total Sales in Rowlett Bikes by Year-Month**
SQL Query: Aggregates total sales by year and month for 'Rowlett Bikes'.

Data Transformation: Converts year-month to datetime.

Visualization: Line chart showing monthly sales over time.

## Question 6
**Staff with highest number of orders**

SQL Query: Finds the staff member with the highest number of orders.

Result: DataFrame showing staff ID, name, and order count.

## Question 7
**Staff with lowest number of orders**

SQL Query: Finds the staff member with the lowest number of orders.

Result: DataFrame showing staff ID, name, and order count.

# Summary
This code reads bike store data from CSV files, loads it into a SQLite database, runs queries to gather insights, and visualizes the results. It uses pandas for data manipulation, SQLite for database operations, and matplotlib for visualization.
