# Amazon_Vine_Analysis

## Overview
For this project, I analyzed the customer reviews for kitchen products sold on Amazon with special attention to reviews associated with their Vine program. Amazon Vine is a service that allows manufacturers and publishers to receive reviews for their products. Companies provide products to Amazon Vine members, who are then required to publish a review.

I used Google Colab and PySpark to perform the ETL process to extract the Amazon kitchen dataset, transform the data, connect to an AWS RDS instance, and then loaded the transformed data into pgAdmin. I then used PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset.


## Results

### ETL

All data was successfully loaded to pgAdmin as demonstrated in the following four tables. 

![products_table](https://user-images.githubusercontent.com/90162669/149632173-d641bb02-81c6-480a-99f1-205e80baf769.png)


![customer_table](https://user-images.githubusercontent.com/90162669/149632182-e7a7ab00-254b-4f56-8063-08025a8e8161.png)


![review_id_table](https://user-images.githubusercontent.com/90162669/149632255-4fe63d61-ec10-4562-bb16-0c9eda8be8c1.png)


![vine_table](https://user-images.githubusercontent.com/90162669/149632257-4a078307-d527-4db8-ae37-cf87fb5e7e57.png)


### Analysis of Vine Reviews

- In this dataset, there were 1207 Vine reviews and 97,810 non-Vine reviews.
- There were 509 Vine reviews with 5 stars and 45,846 non-Vine reviews with 5 stars.
- The percentage of Vine reviews with 5 stars is 42% while the non-Vine reviews with 5 stars was 47%.


Vine Reviews:

![vine_percentage](https://user-images.githubusercontent.com/90162669/149639925-144e95e0-403c-46dc-a332-3cccf20dbdfa.png)


Non-Vine Reviews: 

![non_vine_percentage](https://user-images.githubusercontent.com/90162669/149639931-c007578c-b196-4b55-97c9-b7106775eb35.png)



## Summary

Reviewers in the Vine program were 5% less likely to offer a 5 star review than non-Vine reviewers. This indicates there is not a positivity bias for Vine reviews. I would recommend comparing 1, 2, 3, and 4 star reviews also for this same dataset. In addition, I think it would be helpful to compare several other datasets to see if these results are consistent with other product types.  



