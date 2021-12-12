# Amazon_Vine_Analysis :lipstick:

## OVERVIEW

This project launches into the world of products reviews, with the ultimate purpose of evaluating if a positivity bias exists when reviewers are compensated for their feedback. The data was taken from Amazon, and includes reviews for products that fall under the "Beauty" category. Included in the dataset are reviews from the Vine program, which provides incentives to a select group of customers in exchange for a product review. 

The analysis includes an ETL process, in which the dataset is first extracted, transformed, connected to an AWS RDS instance, and then loaded into pgAdmin. The analysis portion was completed in Google Colab using PySpark.


## TOOLS & RESOURCES

### SOFTWARE

* Python/PySpark
* Google Colab Notebook
* PostgreSQL 14.0 
* pgAdmin 4
* AWS 

### DATA & CODE

* [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
* PostgreSQL Tables [1](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/0505d67f39c2e11c79a12c9888dadc70b3868a86/Images/customers_table.png), [2](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/0505d67f39c2e11c79a12c9888dadc70b3868a86/Images/products_table.png), [3](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/0505d67f39c2e11c79a12c9888dadc70b3868a86/Images/review_table.png), [4](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/0505d67f39c2e11c79a12c9888dadc70b3868a86/Images/vine_table.png)
* [Amazon_Reviews_ETL.ipynb](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/808f26d8e865d526ed7110dc10b0847ad9d5428c/Amazon_Reviews_ETL.ipynb)
* [Vine_Review_Analysis.ipynb](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/808f26d8e865d526ed7110dc10b0847ad9d5428c/Vine_Review_Analysis.ipynb)

## ANALYSIS & SUMMARY

### RESULTS

As a first step, the data was filtered to select rows where the `total_votes` count is greater than or equal to 20, AND where the ratio of `helpful_votes` divided by `total_votes` is greater than or equal to 50%. This was done to select reviews that are more likely to be helpful (or influential).

#### Total Number of Reviews

![alt_text](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/18ff916817faa07e0ce8950fafe5615d187ff6f2/Images/analysis1.png)

There are `74,702` reviews that meet this criteria.

#### Total Number of 5-star Reviews ⭐

![alt_text](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/18ff916817faa07e0ce8950fafe5615d187ff6f2/Images/analysis2.png)

Next, the total number of 5-star reviews was obtained: `43,408`.

#### Vine Reviews 

![alt_text](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/18ff916817faa07e0ce8950fafe5615d187ff6f2/Images/analysis3.png)

* Total Number of Vine Reviews: `647`
* Total Number of Vine Reviews with a 5-Star rating ⭐: `229`
* Percentage of Vine Reviews with a 5-Star rating ⭐: `35.39%`

#### Non-Vine Reviews 

![alt_text](https://github.com/farwaali08/Amazon_Vine_Analysis/blob/18ff916817faa07e0ce8950fafe5615d187ff6f2/Images/analysis4.png)

* Total Number of Non-Vine Reviews: `74,055`
* Total Number of Non-Vine Reviews with a 5-Star rating ⭐: `43,179`
* Percentage of Non-Vine Reviews with a 5-Star rating ⭐: `58.31%`

### SUMMARY

About `35%` of Vine reviews were 5 stars, which, while being a fair margin, is considerably lower than the ratio for the non-Vine reviews, at approximately `58%`. Additionally, roughly `99.5%` of all reviews with a 5-star rating can be attributed to non-Vine reviewers, which suggests that a positivity bias towards reviews in the Vine program does **not** exist. The data suggests that Vine reviewers may actually be more critical in their feedback than their counterparts.

For further review, it would be interesting to conduct a meta-analysis across the different product sub-categories. The "Beauty" category in itself encompasses thousands of different products and brands, which explains the large number of total reviews. Interestingly, only `0.9%` of all Beauty reviews came from the Vine program, and it would be helpful to see how the reviews are distributed amongst the different product categories. It would also be helpful to produce a list of products that are reviewed by both Vine and non-Vine reviewers, and determine an average Vine and non-Vine rating for each product.
