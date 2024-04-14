# Home Sales Data Analysis

## Overview
This project analyzes home sales data using PySpark SQL to determine key metrics such as average prices for different types of homes and sales trends over the years. The analysis includes creating temporary views, partitioning data, caching tables, and measuring query runtimes.

## Files
Home_Sales.ipynb: Jupyter Notebook containing the PySpark SQL analysis
home_sales_revised.csv: Dataset containing home sales data

## Setup
Clone the repository to your local machine.
Install the necessary dependencies, including PySpark.

## Data Loading
The home_sales_revised.csv data is loaded into a Spark DataFrame.

## Temporary Table

A temporary table named "home_sales" is created from the DataFrame for easy querying.

## Questions and Findings

Average Price for Four-Bedroom Houses Sold Each Year

Query: Calculate the average price for a four-bedroom house sold for each year.
Finding: The average price for four-bedroom houses varies from year to year, with some years showing higher prices due to market conditions or other factors.

Average Price of Homes with Three Bedrooms and Three Bathrooms Each Year

Query: Calculate the average price of a home for each year the home was built, with three bedrooms and three bathrooms.
Finding: Homes with three bedrooms and three bathrooms tend to have consistent average prices across different years, indicating a stable market for such properties.

Average Price of Homes with Specific Criteria Each Year

Query: Calculate the average price of a home for each year the home was built, with three bedrooms, three bathrooms, two floors, and a size greater than or equal to 2,000 square feet.
Finding: Homes with these specific criteria command higher average prices, likely due to their desirable features and larger sizes.

Average Price of Homes per "View" Rating

Query: Calculate the average price of a home per "view" rating, with an average home price greater than or equal to $350,000.
Finding: Homes with higher "view" ratings tend to have higher average prices, especially when the average home price is above $350,000.

## Data Partitioning
The data is partitioned by the "date_built" field and stored in parquet format for efficient querying.

## Cached Table

The "home_sales" table is cached for faster access to the data.

## Query Runtimes
The runtime for queries is measured to compare performance between cached and uncached data.

## Uncaching Table
The "home_sales" table is uncached to release memory resources.

## Conclusion
This project demonstrates the use of PySpark SQL for analyzing home sales data, showcasing the ability to derive meaningful insights from large datasets efficiently.
