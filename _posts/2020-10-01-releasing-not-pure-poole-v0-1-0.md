---
layout: post
title: Prediction of diabetes using scikit-learn
author: ChenSiting
tags:
- machine learning
- data analysis
- data cleaning
- data visualization
date: 2025-02-01 13:56 +0800
last_modified_at: 2025-03-30 11:08:25 +0800
---

This project uses the UCI diabetes dataset to build and evaluate machine learning models for diabetes risk prediction, with a focus on data preprocessing, model comparison, and data-driven decision support for early screening.

## Table of Contents

- [Project Description and Goal](#project-description-and-goal)
- [Model Selection and Training](#model-selection-and-training)
- [Result Analysis](#result-analysis)
- [Personal Reflection](#personal-reflection)

## Project Description and Goal

Diabetes is a chronic metabolic disease. Traditional prediction methods based on static factors such as age and gender often have limited accuracy. Using scikit-learn and multiple machine learning algorithms, I built and compared diabetes prediction models to improve prediction accuracy and support early screening and intervention. The dataset contains eight features, including number of pregnancies, glucose level, and blood pressure. I compared model performance and selected a high-quality, interpretable model suitable for diabetes prediction.

## Data Preparation and Modeling

I performed data cleaning, outlier removal, and feature standardization on the UCI diabetes dataset. To reduce sampling bias, I used stratified sampling to split the data into training and test sets at a 78:22 ratio. I implemented seven models: Logistic Regression, Random Forest, Decision Tree, SVC, Bagging, AdaBoost, and Gradient Boosting. I applied 5-fold cross-validation and evaluated model performance using cross-validation scores, training and test accuracy, precision, recall, and F1-score.

![数据集分割图](/images/Split.png)

## Result and Analysis

Logistic Regression showed stable performance: a cross-validation score of 76.83%, training accuracy of 76.13%, and test accuracy of 81.66%. The values were close, indicating no obvious overfitting. Random Forest reached 100% training accuracy, but the gap between its cross-validation score (77.09%) and test accuracy (80.47%) suggested a risk of overfitting. Decision Tree had the most severe overfitting: 100% training accuracy but only 72.19% test accuracy. In addition, the classification reports showed that most models had low recall for the disease class (Outcome = 1). For example, Logistic Regression had a recall of 61% for Class 1, indicating that the models’ ability to identify disease samples still needed improvement.

Overall, Logistic Regression delivered the best comprehensive performance. It balanced high test accuracy (81.66%), no obvious overfitting, and high interpretability, making it suitable for initial diabetes prediction. Among ensemble methods, Bagging and AdaBoost showed good generalization, while Gradient Boosting achieved balanced and stable performance with 76.92% test accuracy; these ensemble models could serve as alternative options. Although SVC produced relatively consistent scores across datasets, its overall accuracy was lower and its practical value was limited. Due to severe overfitting, Decision Tree was difficult to apply in real scenarios.

*Logistic Regression Result Graph*
![Logistic Regression结果图](/images/model-result-2.png)

*Random Forest Result Graph*
![Random Forest结果图](/images/model-result-3.png)

*Decision Tree Result Graph*
![Decision Tree结果图](/images/model-result-4.png)

*Bagging Result Graph*
![Bagging结果图](/images/model-result-5.png)

*AdaBoost Result Graph*
![AdaBoost结果图](/images/model-result-6.png)

*GradientBoosting Result Graph*
![GradientBoosting结果图](/images/model-result-7.png)

*SVM Result Graph*
![SVC结果图](/images/model-result-8.png)

## Personal Reflection

Through this project, I learned core machine learning concepts and practical methods for medical data analysis, including algorithm application and parameter tuning for Logistic Regression and Random Forest, and how to align model performance with real medical needs. This project strengthened my skills in data preprocessing, model evaluation, overfitting control, and medical data analysis.
