# Home Sales Data Analysis with PySpark

## Project Overview

This project analyzes residential home sales data using **PySpark** and **SparkSQL** to identify pricing trends and demonstrate scalable data processing techniques.

The goal was not only to query housing data, but to show how large datasets can be transformed into meaningful business insights that could support:

- property valuation decisions  
- market trend analysis  
- investment strategy  
- operational efficiency in data workflows  

This project highlights my ability to combine **data engineering practices** with **business-focused analysis**.

---

## Business Problem

Real estate datasets can contain millions of records, making traditional analysis tools slow or inefficient.

The challenge was to:

- process a large housing dataset efficiently  
- analyze price drivers across home features  
- improve query performance for repeated analysis  
- present findings that stakeholders can understand  

---

## Business Value Delivered

Using distributed data processing, this project demonstrates how data can be used to answer key business questions such as:

- What home features drive higher sale prices?
- Do newer homes sell for more?
- How much does a premium view increase value?
- How can data storage choices improve reporting speed?

The analysis can help organizations:

- better estimate property values  
- identify market opportunities  
- reduce reporting time  
- improve scalability of analytics workflows  

---

## Technical Skills Demonstrated

### Data Analysis
- Exploratory data analysis
- SQL-based aggregation
- Trend identification
- Performance benchmarking

### Data Engineering
- Distributed computing with Spark
- Data caching
- Partitioned parquet storage
- Cloud-based data ingestion

### Tools & Technologies
- Python
- PySpark
- SparkSQL
- AWS S3
- Jupyter Notebook / Google Colab

---

## Dataset

The dataset includes:

- Sale price
- Bedrooms
- Bathrooms
- Square footage
- Number of floors
- View rating
- Year built
- Sale date

These variables were used to evaluate how property characteristics influence pricing.

---

## Key Questions Answered

### 1. How do home features impact sale price?
The project measures average sale price by:
- bedrooms
- bathrooms
- living space
- number of floors

### 2. Does view quality affect value?
Properties with stronger view ratings were compared to determine price differences.

### 3. Can performance be improved?
Query runtime was measured before and after:
- caching
- parquet partitioning

---

## Key Findings

### Pricing Insights
- Larger homes consistently sold at higher prices  
- Additional bathrooms increased average property value  
- Premium views significantly increased home sale prices  
- Newer homes showed stronger pricing performance in many segments  

### Technical Insights
- Caching reduced repeated query execution time  
- Partitioned parquet files improved read performance  
- Spark handled large-scale aggregation efficiently  

---

## Example Insight

One of the analyses showed that homes with higher view ratings sold at substantially higher average prices, suggesting that visual desirability can be a measurable pricing factor in residential markets.

This type of analysis could support:
- appraisal teams  
- investment firms  
- real estate analysts  

---

## Project Workflow

### 1. Load Data
Imported the dataset directly from cloud storage into Spark.

### 2. Clean Data
Validated and converted column data types for analysis.

### 3. Analyze Data
Used SparkSQL to answer business questions.

### 4. Optimize Performance
Compared runtime across:
- uncached data
- cached data
- parquet data

### 5. Interpret Results
Converted technical output into business insights.

---

## Sample SQL Query

```sql id="hf9z2j"
SELECT
    bedrooms,
    bathrooms,
    ROUND(AVG(price), 2) AS avg_price
FROM home_sales
GROUP BY bedrooms, bathrooms
ORDER BY bedrooms, bathrooms;
