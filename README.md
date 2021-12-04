# Amazon Vine Analysis

## Purpose of the Analysis
In this project, I perform ETL (Extract, Transform, Load) analysis on Amazon Vine reviews of furniture products sold on Amazon.com and assess whether there is any positive bias from Amazon Vine reviewers. The analysis is done in broadly two steps:

1) PySpark is used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin.  

2) PySpark used to determine if there is any bias toward favorable reviews from Vine members in your dataset. 

### Background of Amazon Vine Program
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like "SellBy" pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

### Resources
Tools used: PySpark, Google Colab Notebooks, AWS RDS, PostgreSQL, pgAdmin 

Data sources: [Amazon Vine furniture reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Furniture_v1_00.tsv.gz) 

## Results
The following questions are answered in the screenshot below:

- How many Vine reviews and non-Vine reviews were there?

- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

![results_summary](/Images/results_summary.png)

## Summary
There is a modest positivity bias for reviews in the Vine program. Among the unpaid users ~47% reviewers gave 5 star reviews vs among the Amazon Vine users ~54% reviewers gave 5 star reviews for furniture product. However, sample size of Amazon Vine reviews was 136, much smaller than 17,999 unpaid users. 

As additional analysis one could do a statistical test to see if the difference is statistically significant. 

## Additional Images of Data Tables Imported in PostgresSQL
Customers table

![customers_table](/Images/customers_table.png)

Products table

![products_table](/Images/products_table.png)

Review ID table

![review_id_table](/Images/review_id_table.png)

Vine table

![vine_table](/Images/vine_table.png)
