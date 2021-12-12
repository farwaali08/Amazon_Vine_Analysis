# Amazon_Vine_Analysis :lipstick:

## OVERVIEW

This project launches into the world of products reviews, with the ultimate purpose of evaluating if a bias is observed when reviewers are compensated for their feedback. The data was taken from Amazon, and includes reviews for products that fall under the "Beauty" category. Included in the dataset are reviwes from the Vine program, which provides incentives to a select group of customers in exchange for a product review. 

The analysis includes an ETL process, in which the dataset is first extracted, transformed, connected to an AWS RDS instance, and then loaded into pgAdmin. The analysis portion was completed in Google Colab using PySpark.


## TOOLS & RESOURCES

### SOFTWARE

* Python/PySpark
* Google Colab Notebook
* PostgreSQL 14.0 
* pgAdmin 4
* AWS 

### DATA

* [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
* PostgreSQL Tables [1](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/0505d67f39c2e11c79a12c9888dadc70b3868a86/Images/customers_table.png), [2](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/0505d67f39c2e11c79a12c9888dadc70b3868a86/Images/products_table.png), [3](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/0505d67f39c2e11c79a12c9888dadc70b3868a86/Images/review_table.png), [4](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/0505d67f39c2e11c79a12c9888dadc70b3868a86/Images/vine_table.png)
* Code
* [Amazon_Reviews_ETL.ipynb](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/808f26d8e865d526ed7110dc10b0847ad9d5428c/Amazon_Reviews_ETL.ipynb)
* [Vine_Review_Analysis.ipynb](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/808f26d8e865d526ed7110dc10b0847ad9d5428c/Vine_Review_Analysis.ipynb)

## ANALYSIS & SUMMARY

### RESULTS

As a first step before the analysis, the review data was 

![alt_text](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/18ff916817faa07e0ce8950fafe5615d187ff6f2/Images/analysis1.png)

![alt_text](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/18ff916817faa07e0ce8950fafe5615d187ff6f2/Images/analysis2.png)

![alt_text](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/18ff916817faa07e0ce8950fafe5615d187ff6f2/Images/analysis3.png)

![alt_text](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/18ff916817faa07e0ce8950fafe5615d187ff6f2/Images/analysis4.png)

### SUMMARY
