# Credit_Risk_Analysis

## Overview of the analysis - Explain the purpose of this analysis

The purpose of this analysis is to explore various methods for predicting credit risk using machine learning models. In order to best analyze credit risk, 6 different machine learnign models are trained and tested using the same loan dataset. The performance of each model, as demonstrated by balanced accuracy, precision and recall scores, is used to evaluate which model(s) ***is/are*** best suited to conduct credit risk analysis.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

- There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models

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
  - Balanced accuracy score: .67
  - Precision scores:
    - high_risk: .01
    - low_risk: 1.00
  - Recall scores:
    - high_risk: .72
    - low_risk: .61

![SMOTEENN-scores-img](<readme-imgs/output-imgs-resized/smoteenn-resampling.png>)

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

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning

- There is a summary of the results
- There is a recommendation on which model to use, or there is no recommendation with a justification
