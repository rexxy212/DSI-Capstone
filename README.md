# Executive Summary
Product reviews are an essential part of any business. Moreso, for e-commerce
sites since pictures and descriptions provided by the sellers may not be an
accurate representation of a product. As there are no other ways for consumers
to verify or try products out, reviews become an important supplement
source of information.

Due to Shopee's incentivised review policy, many people leave reviews to simply
hit the target word count requirements, without any fruiful contribution to the
review of the actual product.

Exploratory data analysis was performed on dataset of 10000 positive Shopee
reviews to glean some insight into which words frequently appeared and whether
these reviews were legitimate.

A sample of 1000 reviews were then manually labelled as real or fake reviews and
Pycaret was deployed to perform modeling and optimisation.

Logistic Regression on CountVectorized unigram performed the best overall with a
baseline AUC score of 0.8497 and F1 score of 0.8529. The model was then tuned
with a random CV search, and the finalized model had a test AUC score of 0.9732
and F1 score of 0.9432.

# Problem Statement
As a 3rd party analyst on business improvements, we aim to detect real and fake
reviews using Natural Language Processing (NLP) by analysing data from pulled
from Shopee’s site.

# Content
1. Data Cleaning & Exploratory Data Analysis
2. Modeling

# Conclusions
The relatively high test AUC score of 0.9732 and F1 score of 0.9432 attained
indicated that tuned Logistic Regression model is quite successful in
predicting whether review is legitimate or not based on the text.

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**label**|*int*|shopee_reviews.csv|Rating of review.|
|**text**|*object*|shopee_reviews.csv|Comment of review.|
|**text_length**|*int*|shopee_reviews.csv|Number of words in the text.|
|**real_review**|*object*|train.csv|Indicator of whether a review is legitimate.|

# Credits
Shopee Text Reviews [Source](https://www.kaggle.com/shymammoth/shopee-reviews)
