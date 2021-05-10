# Credit_Risk_Analysis

## Overview

The purpose of this analysis is to explore various methods for predicting credit risk using machine learning models. In order to best analyze credit risk, six different machine learning models are trained and tested using the same loan dataset. The performance of each model, as demonstrated by balanced accuracy, precision and recall scores, is used to evaluate which model is best suited to handle the unbalanced classification problem inherent in credit risk analysis.

## Results

- RandomOverSampler
  - Balanced accuracy score: .65
  - Precision scores:
    - high_risk: .01
    - low_risk: 1.00
  - Recall scores:
    - high_risk: .72
    - low_risk: .59

![RandomOverSampler-scores-img](<readme-imgs/output-imgs-resized/naive-random-oversampling.png>)

- SMOTE
  - Balanced accuracy score: .66
  - Precision scores:
    - high_risk: .01
    - low_risk: 1.00
  - Recall scores:
    - high_risk: .63
    - low_risk: .69

![SMOTE-scores-img](<readme-imgs/output-imgs-resized/smote-oversampling.png>)

- ClusterCentroids
  - Balanced accuracy score: .54
  - Precision scores:
    - high_risk: .01
    - low_risk: 1.00
  - Recall scores:
    - high_risk: .69
    - low_risk: .40

![ClusterCentroids-scores-img](<readme-imgs/output-imgs-resized/cluster-centroids.png>)

- SMOTEENN
  - Balanced accuracy score: .65
  - Precision scores:
    - high_risk: .01
    - low_risk: 1.00
  - Recall scores:
    - high_risk: .71
    - low_risk: .58

![SMOTEENN-scores-img](<readme-imgs/output-imgs-resized/smotenn-corrected.png>)

- BalancedRandomForestClassifier
  - Balanced accuracy score: .79
  - Precision scores:
    - high_risk: .03
    - low_risk: 1.00
  - Recall scores:
    - high_risk: .70
    - low_risk: .87

![BalancedRandomForestClassifier-scores-img](<readme-imgs/output-imgs-resized/balanced-random-forest.png>)

- EasyEnsembleClassifier
  - Balanced accuracy score: .93
  - Precision scores:
    - high_risk: .09
    - low_risk: 1.00
  - Recall scores:
    - high_risk: .92
    - low_risk: .94

![EasyEnsembleClassifier-scores-img](<readme-imgs/output-imgs-resized/easy-ensemble.png>)

## Summary

Having measured the performance of all six of the machine learning models, it is clear that ensemble models are superior in their evaluation of credit risk. Oversampling with the RandomOverSampler and SMOTE algorithms, undersampling with the ClusterCentroids algorithm and the combinatorial method of over and undersampling with the SMOTEENN algorithm all generated mediocre results. Only when leveraging ensemble classification to reduce bias by using the BalancedRandomForestClassifier algorithm and the EasyEnsembleClassifier algorithm did the models produce high scores for most metrics.

The EasyEnsembleClassifier performed best across all the metrics evaluated with a balanced accuracy score of .93, precision scores of .09 and 1.00 for high risk and low risk respectively, and recall scores of .92 and .94 for high risk and low risk respectively. Given its relative performance in evaluating high and low risk loans the EasyEnsembleClassifier is the clear recommendation for which model to use for analyzing credit risk.

A particularly important aspect of the EasyEnsembleClassifier algorithm's scores is the high risk recall value of .92. Compared to all the other models a significantly smaller percentage of high risk loans failed to be flagged as such. Furthermore, the EasyEnsembleClassifier algorithm did not trade this high recall for precision relative to the other algorithms tested. The high risk recall outperformance is so significant because the inability to identify risky loans can easily lead to a financial institution's collapse if the number of non-performing loans on its balance sheet is perceived to be much lower than it actually is.

One item of note is that all six models had very low precision scores for high risk loans. While the nature of credit risk data and its analysis might limit the ability to improve that metric, further exploration of the high risk precision score is warranted. An analysis of the features and underlying data to best understand the low score could highlight the need to reevaluate features and their data and in turn improve precision and model performance overall. Even if the precision cannot be raised without causing the recall score to decrease, there is still more analysis to be conducted. While it is important to capture as many potential non-performing loans as possible, there may be a higher cost to creating subscription barriers for low risk borrowers. If too many low risk borrows are classified as high risk and decided to go to a competing institution, the cost of lost business might outweigh the benefits of identifying such a high percentage of high risk loans. 
