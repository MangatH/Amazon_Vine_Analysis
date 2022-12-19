# Amazon_Vine_Analysis

## Overview of the analysis:
This project involves analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
In this project, with the access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. I pickup the dataset related to the reviews in the category 'baby products'. 

### Objectives:
* Use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 
* Use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. 
* Write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

### Deliverables:
* Deliverable 1: Perform ETL on Amazon Product Reviews
* Deliverable 2: Determine Bias of Vine Reviews
* Deliverable 3: A Written Report on the Analysis (README.md)


## Results:
For this analysis, almost 2 million reviews were analysed. These reviews were filtered on various parameters to reduce the size of data for better analysis. <br/>

* First, the dataset was filtered to retrieve the total votes count greater than or equal to 20.
<img width="780" alt="Screen Shot 2022-12-19 at 6 46 56 PM" src="https://user-images.githubusercontent.com/111387025/208440226-2c4044d4-c9ff-4047-9187-2fd949b42d88.png">

* Further, the data was filtered where the number of helpful_votes divided by total_votes is equal to or greater than 50%.

<img width="867" alt="Screen Shot 2022-12-19 at 6 48 21 PM" src="https://user-images.githubusercontent.com/111387025/208440772-0fb677b0-bd07-4ea0-bd49-369ead579782.png">

* A new dataframe was created that retrieved all the rows where a review was written as part of the Vine program.

<img width="842" alt="Screen Shot 2022-12-19 at 6 49 11 PM" src="https://user-images.githubusercontent.com/111387025/208441067-2ce005e5-236c-4db8-b524-9a3e7b6fc6dd.png">

* Another dataframe was created which retrieved all the rows where the review was not part of the Vine program.

<img width="857" alt="Screen Shot 2022-12-19 at 7 10 14 PM" src="https://user-images.githubusercontent.com/111387025/208441259-73b4f937-9d67-453a-8448-b02eec2d4b01.png">

* In the final step of the analysis, the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review were determined.

<img width="600" alt="Screen Shot 2022-12-19 at 7 11 11 PM" src="https://user-images.githubusercontent.com/111387025/208441554-f099130c-68bb-4e4d-920d-0275668a3835.png">

#### Question 1: How many Vine reviews and non-Vine reviews were there?
The total number of Vine reviews were 463, which were only 1.8 percent of total reviews. <br/>
In contrast, non-Vine reviews were 25,079, a little more than 98 percent of total reviews.

#### Question 2: How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
There were 202 5 star Vine reviews. <br/>
12,028 non-Vine reviews were 5 stars.

#### Question 3: What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
The percentage of Vine reviews which were 5 stars were 43.63 percent. <br/> 
The percentage of non-Vine reviews which were 5 stars were 47.96 percent.


## Summary
The analysis did not indicate any bias for reviews in the Vine program as the percent of 5 star votes in both categories were quite close i.e. 43.63 percent Vine reviews and 47.96 percent non-Vine reviews. <br/>

<img width="600" alt="Screen Shot 2022-12-19 at 7 11 11 PM" src="https://user-images.githubusercontent.com/111387025/208447574-e5006dd4-c036-4e9d-bd55-506f73ccac5b.png">

However, the study highlighted that the reviewers in the Vine program were more careful while giving the reviews in contrast to the non-Vine reviews.<br/>
Another significant aspect of the analysis is that the data was filtered before making the final analysis. Therefore, attempt can be made to include a larger dataset for the final analysis. <br/>
Furthermore, analysis can be done on the other datasets as well, to ensure a concrete evidence on the conclusion drawn from this study.



