# Wine Origination Prediction using baseline, bagging, boosting, and stacked models.
![My Skills](https://skillicons.dev/icons?i=python)

## Introduction
This project delves into the domain of oenology, the science of wine and winemaking, to predict the region of origin for wines based on their chemical composition. By constructing and comparing fourteen different models across various ensemble methods—bagging, boosting, and stacking—this work aims to achieve the highest accuracy in regional prediction.

## Overview
We approach the problem by creating four baseline models (Random Forest, kNN, SVC, Logistic Regression), four bagging models using the same base learners, four boosting models (Ada Boost, Gradient Boost, XG Boost, Ensemble), one stacked model combining the base learners with a Logistic Regression meta-classifier, and a final stacked model with hyperparameters tuned via Grid Search Cross-Validation. The ensemble methods are chosen for their proven effectiveness in enhancing model performance, with the stacking approach particularly noted for increasing prediction accuracy.

## Data
The dataset comprises the results of a chemical analysis of wines grown in three distinct regions, with 178 samples in total. The thirteen variables representing the wine's characteristics are alcohol, malic acid, ash, alkalinity of ash, magnesium, total phenols, flavonoids, nonflavonoid phenols, proanthocyanins, color intensity, hue, od280/od315 of diluted wines, and proline.

## Libraries and Tools Used
mlxtend for implementing stacking classifiers
xgboost for the XG Boost algorithm
sklearn for various classifiers and cross-validation
matplotlib and seaborn for visualizations
pandas for data manipulation
numpy for numerical operations
Exploratory Data Analysis (EDA)
The EDA is focused on understanding the distribution and relationships of the variables through descriptive statistics, pair plots, and correlation analysis, ensuring there are no missing values.

## Models
A variety of ensemble techniques are applied:

- Bagging to reduce variance using classifiers like RandomForest and kNN.
- Boosting to reduce bias with AdaBoost, Gradient Boost, and XGBoost.
- Stacking to improve prediction accuracy with a combination of models as base learners and a meta-classifier for final predictions.
- Stacking with Grid Search CV for hyperparameter tuning to optimize model performance.

## Results
The models are evaluated based on their accuracy, with a particular interest in how ensemble methods compare to their base learners. Notably, the stacking models show promising results, especially with grid search cross-validation.

## Conclusion
The project concludes with the stacked model with Grid Search Cross Validation emerging as the most accurate, achieving a near-perfect prediction score. However, considering the computational cost and time, the marginal improvement in accuracy over simpler models like SVC is questioned, underlining the importance of balancing model complexity with practical utility. The findings underscore the potential of ensemble methods in predictive modeling, with applications extending beyond oenology to any field where precision is paramount.

## Setup and Execution
1. Data is preprocessed and scaled for uniformity.
2. Various ensemble models are constructed and trained.
3. The models are evaluated and compared based on cross-validation scores.
4. The best-performing model is identified for predicting the wine's region of origin.

## Future Work
The project highlights areas for further improvement, such as refining the stacked models or exploring alternative ensemble techniques. The adaptability of the approach suggests its applicability in other high-stakes prediction scenarios, such as medical diagnoses or safety-critical systems.
