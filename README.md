# Home Sales Data Analysis

This project investigates trends in home sales by analyzing a dataset containing detailed property information. The goal is to understand pricing patterns for various home types and features over time.

---

## Who Will Benefit and Why

Real estate professionals, market analysts, and prospective homebuyers can benefit from this analysis. It provides insights into how home attributes such as bedroom count, bathrooms, size, and view quality influence average sale prices, helping stakeholders make informed decisions.

---

## Dataset

The analysis uses a comprehensive dataset (`home_sales_revised.csv`) containing home sales records, including features like number of bedrooms, bathrooms, floors, year built, size, and sale price.

---

## Methodology

* Loaded the dataset into a Spark DataFrame using PySpark.
* Created a temporary SQL table named `home_sales` for efficient querying.
* Performed queries to calculate average home prices based on different criteria such as bedroom count, bathrooms, floors, size, and view rating.
* Partitioned the dataset by the `date_built` field and stored it in Parquet format for faster access.
* Cached the `home_sales` table to improve query performance and measured runtime differences between cached and uncached states.
* Released cached data after analysis to free resources.

---

## Key Findings

* **How do average prices for four-bedroom houses vary over the years?**
  Prices fluctuate year-to-year, reflecting market dynamics and external factors impacting housing demand.

* **What is the pricing trend for homes with three bedrooms and three bathrooms by year built?**
  These homes maintain relatively stable average prices, indicating steady demand in this segment.

* **Do homes with three bedrooms, three bathrooms, two floors, and size ≥ 2,000 sq ft command higher prices?**
  Yes, such homes consistently achieve higher average prices, likely due to their larger size and desirable features.

* **Does a higher "view" rating correlate with higher home prices?**
  Homes with better views tend to have higher average prices, particularly when prices exceed \$350,000.

* **How does caching affect query performance?**
  Caching the data significantly reduces query runtimes, improving efficiency for repeated analyses.

---

## Conclusion

The project successfully demonstrates how PySpark SQL can be applied to large real estate datasets to extract actionable insights about home pricing trends. It highlights the influence of home features and market conditions on sale prices and shows the benefits of data partitioning and caching for performance optimization.

---

## Recommendations

Expanding the dataset to include additional geographic regions or more recent sales data could further improve the analysis. Incorporating advanced machine learning models may also help predict future pricing trends.

---

## Files

* `Home_Sales.ipynb`: Jupyter Notebook with the PySpark SQL analysis
* `home_sales_revised.csv`: Dataset containing detailed home sales data
