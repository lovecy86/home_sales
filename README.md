# Home Sales Analysis Using PySpark
## Overview
This project analyzes real estate sales data using Apache Spark and SparkSQL. The goal is to extract key insights about home prices across various attributes such as number of bedrooms, bathrooms, square footage, and view ratings.

## Technologies Used
* PySpark
* SparkSQL
* AWS S3 (for data access)
* Colab 

## Project Tasks Summary
* 1. Loaded home sales data from an AWS S3 bucket into a PySpark DataFrame.

* 2. Created a temporary SQL table (home_sales) for querying.

* 3. Answered key analytical questions using SparkSQL, including:

    * Average price of 4-bedroom homes sold per year.

    * Average price of 3-bedrooms and 3-bathroom homes per year built.

    * Average price of 3-bedrooms, 3-bathrooms, 2-floor,  homes ≥ 2000 sq ft by year built.

    * Average home price per view rating (only for homes ≥ $350,000).

* 4. Cached the temporary table and compared the query runtime before and after caching.

* 5. Partitioned the data by date_built and saved it in Parquet format for optimized performance.

* 6. Created a temporary view from the partitioned data and reran queries to compare performance.

* 7. Uncached the temporary table and verified it using PySpark methods.

## Insights
From the analysis, it is found that cached execution is the fastest, partitioning is faster and uncached is the slowest.
![cached](cached.png)                    ![partitioned](partitioned.png)                        ![uncached](uncached.png)