# Overview
This project was focused on identifying the best analytical model for predicting customer churn in telecommuincations. A secondary goal was to 
determine the best approach to handling missing data, comparing PPM, CART and LASSO imputation methods. The dataset for this model are largely categorical data. 
Interestingly, this project mirrors a real-world project to reduce long distance customer 
churn using various incentives completed when I worked for GTE Corporation / Verizon.

# Notes
:heavy_check_mark: Six different analytical models were evaluated for their predictive accuracy, including K-Nearest Neighbors, Boosting/Bagging, Decision Trees, Stepwise Logistic Regression, Random Forests and Naive Bayes. 

:heavy_check_mark: Three different approaches to imputing missing data were tested and evaluated, including predictive mean matching (PPM), classificatoin and regression trees (CART), least absolute shrinkage and selection operator
 (LASSO).  Missing data is a very common problem is analytics/AI.

:heavy_check_mark: Balancing the data in classification prediction is extrememly important, though the research on balancing data often deals with rare occurrences (e.g. bank fraud, cancer detection, intrusion detection) in a data set. In this analysis both under-sampling and over-sampling were evaluated.
