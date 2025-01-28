# HOME SALES

Overview
This document provides details about the SQL queries used to analyze the home sales dataset in PySpark. The queries aim to extract insights, such as average home prices based on various criteria, while leveraging Spark SQL's capabilities for big data processing.

The queries also demonstrate performance optimization techniques, including caching and partitioning.

Queries
1. Average Price for Four-Bedroom Houses Sold Per Year
Description: Calculates the average price of four-bedroom houses sold, grouped by year, and rounded to two decimal places.

2. Average Price of 3-Bedroom, 3-Bathroom Houses Per Build Year
Description: Calculates the average price of homes with 3 bedrooms and 3 bathrooms, grouped by the year the home was built.

3. Average Price of 3-Bedroom, 3-Bathroom, 2-Floor Houses ≥ 2,000 Square Feet
Description: Calculates the average price of homes with specific attributes: 3 bedrooms, 3 bathrooms, 2 floors, and at least 2,000 square feet.

4. Average Price Per "View" Rating (≥ $350,000)
Description: Calculates the average home price per "view" rating, showing only ratings with an average price ≥ $350,000. Results are sorted by descending view rating.

5. Partitioning by date_built (Output Data)
Description: Saves the home sales data in Parquet format, partitioned by the date_built column.

6. Query on Partitioned Parquet Data
Description: Reads the partitioned Parquet data and runs the same query as #4 to calculate the average price per "view" rating, filtering for average prices ≥ $350,000.

# How to Run These Queries
1. Set Up the Environment:
- Install PySpark and Java.
- Create a SparkSession and configure the environment variables.

2. Load the Data:
- Load the home_sales_revised.csv file into a DataFrame.

3. Create Temporary Views:
- Use .createOrReplaceTempView() to create SQL views for the loaded or processed data.

4. Execute Queries:
- Run each query with spark.sql() and display the results using .show().

5. Optimize:
- Cache tables and/or partition the data in Parquet format for faster query execution.
