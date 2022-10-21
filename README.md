# Amazon_Vine_Analysis

## Analysis Overview
Big Data ETL using AWS RDS and PostgreSQL, and used PySpark to investigate whether Amazon Vine reviews are free of bias.
The analysis uses PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, load the transformed data into pgAdmin and calculate different metrics.
We focused on the US reviews for video games.

## Resources
### Data Source: 
* Amazon Review datasets,

### Software: 
* Google Colab Notebook, 
* PostgreSQL 11.9, 
* pgAdmin 4, 
* AWS- RDS and S3
## Roadmap
The first step was to extract the dataset from an AWS S3 using PySpark in order to transform it and load it to AWS again. Please refer to Amazon_Reviews_ETL.ipynb to see the code. Note that I downloaded it as a jupyter notebook file, but it was originally created in Google Colab for PySpark to run. I basically divided the whole dataframe into 4 smaller dataframes for better analysis. These dataframes were then loaded to AWS RDS using a a connection from PySpark to PostgreSQL.

## Results
### Paid Vine Program

* 613 total reviews
* 222 5-star reviews
* 36.2% of vine reviews were 5-star
### Unpaid reviews

* 64,968 total reviews
* 30,543 5-star reviews
* 47% of unpaid reviews were 5-star

## Summary
There are total 65,581 helpful revies. The majority of reviews are  unpaid around 99% and 47% of them are 5-star reviews. whereas, only 613 reviews are from vine program and only 36% of them are 5-star revies. As the percentage of 5-star reviews is more in non-vine program as comapred to vine program, there is no positivity bias for reviews in the Vine program.
Additionally we could analyse the statistical distribution (mean, median and mode) of the star rating for the Vine and non-Vine revie
