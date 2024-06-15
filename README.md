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

The attached  code performs data extraction, transformation, loading (ETL), and analysis on a dataset of a bike store. The dataset is first loaded from CSV files into pandas DataFrames, then transferred into a SQLite database. Various SQL queries are executed on the database to retrieve insights, and the results are visualized using matplotlib.




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

6. Analysis and Visualization
Number of Stocks Based on Category and Store
SQL Query: Aggregates total stock quantity by category and store.

Data Transformation: Converts store and category names to categorical data.
Visualization: Bar chart showing stocks per category for each store.
Number of Order Items Based on Category and Store

Data Transformation: Converts store and category names to categorical data.

Visualization: Bar chart showing order items per category for each store.

Total Sales in Santa Cruz Bikes by Year-Month
SQL Query: Aggregates total sales by year and month for 'Santa Cruz Bikes'.

Data Transformation: Converts year-month to datetime.

Visualization: Line chart showing monthly sales over time.
Total Sales in Baldwin Bikes by Year-Month

SQL Query: Aggregates total sales by year and month for 'Baldwin Bikes'.

Data Transformation: Converts year-month to datetime.

Visualization: Line chart showing monthly sales over time.

Total Sales in Rowlett Bikes by Year-Month
SQL Query: Aggregates total sales by year and month for 'Rowlett Bikes'.

Data Transformation: Converts year-month to datetime.

Visualization: Line chart showing monthly sales over time.
Staff with the Most Orders

SQL Query: Finds the staff member with the highest number of orders.

Result: DataFrame showing staff ID, name, and order count.
Staff with the Least Orders

SQL Query: Finds the staff member with the lowest number of orders.

Result: DataFrame showing staff ID, name, and order count.

Summary
This code reads bike store data from CSV files, loads it into a SQLite database, runs queries to gather insights, and visualizes the results. It uses pandas for data manipulation, SQLite for database operations, and matplotlib for visualization.
