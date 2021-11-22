# Predicting-Employee-Attrition

##### Public Leaderboard : 69
##### Private Leaderboard: 26

## Problem Statement: 
Given the monthly information for a segment of employees for 2016 and 2017 and need to predict whether a current employee will be leaving the organization in the upcoming two quarters (01 Jan 2018 - 01 July 2018) or not.
## Approach:
1. First I have looked for any Null values or outliers and the given data didn't have any,
2. The dataset doesn't have a Target column so I have created it in the following way.
    i.  I have discared any employees who has less than 4 months of data.
    ii. Now for the remaining employees I have aggregated the data but before aggregating I took an important step of aggregating the data from the first month of the employee to         the month before last 3 Months. In this way for an employee who has 10 Months of data only the first 7 months are considered for trainning and 10th month is used to create         Target variable 
## Data Pre-processing/Feature Engineering: 
For the data pre-proceesing I have aggreagted the data of remaining employees on Mean, Median, Max, Min, Standard deviation. My results mainly improved when I have taken the aggreagations of last 3 months of the trainning data of an employee. For Instance, an employee who has data of 20 months, last 3 months were ignored when building the train daa and left with 17 months. Now the aggregation is taken for both 1-17th month and 15th-17h Month since an employee leaving the organization will mostly depend on months before he left
## Model: 
Pycaret was used to selec the best model based on F1 Score. I went with pycaret as I have joined the competition on last day and only had few hours. Catboost came as the top model and based on the feature importnaces I went with that model.
