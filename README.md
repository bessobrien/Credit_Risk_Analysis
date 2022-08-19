# Credit Risk Analysis: Supervised Machine Learning

## Overview of Analysis
The purpose of this analysis was to address the process of determining credit risk. We utilized different techniques to train and evaluate models with unbalanced classes. The data is pull from LnedingClub, a peer-to-peer lending services company. We have oversampled and undersampled the data, as well as used a combinatorial approach using the SMOTEENN algorithm. Finally, we compared two new machine learning models that reduce bias.

Afterwards, we evaluated the performance of these models.

## Results

Here are the models that we employed to look at the data:

1. **Oversampling using RandomOverSampler**

The first confusion matrix from oversampling with RandomOverSampler:
![nrp]()
Note:
*Precision:
    *High Risk: 0.01
    *Low Risk: 1.00
*Recall:
    *High Risk: 0.68
    *Low Risk: 0.62

2. **Oversampling using SMOTE**

The confusion matrix from SMOTE:
![smote]()

Note:
*Precision:
    *High Risk: 0.01
    *Low Risk: 1.00
*Recall:
    *High Risk: 0.63
    *Low Risk: 0.66

3. **Undersampling using ClusterCentroids**

The confusion matrix from CusterCentroids:
![nrp]()

Note:
*Precision:
    *High Risk: 0.01
    *Low Risk: 1.00
*Recall:
    *High Risk: 0.60
    *Low Risk: 0.43

4. **Combination sampling with SMOTEENN**

The confusion matrix from SMOTEENN:
![smoteenn]()

Note:
*Precision:
    *High Risk: 0.01
    *Low Risk: 1.00
*Recall:
    *High Risk: 0.70
    *Low Risk: 0.57

5. **Ensemble classification using BalancedRandomForestClassifier**
The confusion matrix from BalancedRandomForestClassifier:
![balanced]()

Note:
*Precision:
    *High Risk: 0.04
    *Low Risk: 1.00
*Recall:
    *High Risk: 0.67
    *Low Risk: 0.91

6. **Ensemble calssification using EasyEnsembleClassifier**
The confusion matrix from EasyEnsembleClassifier:
![easy]()

Note:
*Precision:
    *High Risk: 0.07
    *Low Risk: 1.00
*Recall:
    *High Risk: 0.91
    *Low Risk: 0.94


## Summary

After reviewing the performance of all these models, we noticed that all of the models had high precision rates for low risk applicants, and low precision for high risk applicants. Of all the models, the EasyEnsembleClassifier had the highest sensitivity(recall) at 0.97 for low risk, and 0.91 for high risk. However, the F1 for high risk for this model still indicated quite a bit of imbalance between sensitivity and precision at 0.14.

Based on these findings, we would recommend to avoid using any of these models, and continue testing further models to find one that provides better results, and a better balance between sensitivity and precision.