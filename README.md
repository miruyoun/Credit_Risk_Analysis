# Credit Risk Analysis

## Overview
In this analysis, I evaluated the performance of machine learning algorithms to figure out credit card risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

What You're Creating

## Results

### Naive Random Oversampling
![random](https://user-images.githubusercontent.com/106292020/192284081-f1bdfcdf-5bd2-4042-b39b-f6deb954dedb.PNG)
* Balanced Accurary Score: 65.7%
* Precision: High risk - 0.01 and Low risk - 1.00
* Recall: High risk - 0.71 and Low risk - 0.60
###  SMOTE Oversampling
![smote](https://user-images.githubusercontent.com/106292020/192284078-e524002c-83f2-4311-a860-2e36390728ff.PNG)
* Balanced Accurary Score: 66.2%
* Precision: High risk - 0.01 and Low risk - 1.00
* Recall: High risk - 0.63 and Low risk - 0.69
### Cluster Centroid
![cluster](https://user-images.githubusercontent.com/106292020/192284064-ca4c6bac-8a14-47c2-8727-ee8c25b07ece.PNG)
* Balanced Accurary Score: 54.4% 
* Precision: High risk - 0.01 and Low risk - 1.00
* Recall: High risk - 0.69 and Low risk - 0.40
### SMOTE-ENN Algorithm
![smoteenn](https://user-images.githubusercontent.com/106292020/192284080-f4929e36-8333-44e1-8337-353b9e87c0e1.PNG)
* Balanced Accurary Score: 64.5%
* Precision: High risk - 0.01 and Low risk - 1.00
* Recall: High risk - 0.72 and Low risk - 0.57
### Balanced Random Forest Classifier 
![balanced](https://user-images.githubusercontent.com/106292020/192284061-7d3c12cc-e245-459f-967a-20bd5ff54e70.PNG)
* Balanced Accurary Score: 78.9%
* Precision: High risk - 0.03 and Low risk - 1.00
* Recall: High risk - 0.70 and Low risk - 0.87
### Easy Ensemble AdaBoost Classifier
![ada](https://user-images.githubusercontent.com/106292020/192284065-226fd321-df50-405b-85d7-ff78786189e3.PNG)
* Balanced Accurary Score: 93.1%
* Precision: High risk - 0.09 and Low risk - 1.00
* Recall: High risk - 0.92 and Low risk - 0.94

## Summary

Most of the machine learning models performed poorly and did not predict credit risk well. The precision of the models was similar or very close and there was also a lot of variation in recall. The oversampling, undersampling, and combination approach had the lowest accuracy and were all below 70%. However, the last two models had the highest accuracies, 78.9% and 93.1%. The balanced random forest model is the best model due to its high recall and decent accuracy, despite having poor precision for high-risk credit accounts. This indicates that, despite predicting many high-risk accounts, majority of them were low-risk accounts. For the companies interests, it is more important for them to identify high-risk accounts, though, so they don't lend money to people who won't be able to repay it.
