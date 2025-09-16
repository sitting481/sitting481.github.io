---
layout: post
title: Prediction of diabetes using scikit-learn
author: Siting Chen
tags:
- machine learning
- scikit-learn
- diabetes prediction
date: 2025-02-19 13:56 +0800
last_modified_at: 2025-03-10 11:08:25 +0800
---

This is a project that uses multiple machine learning models to predict the risk of developing diabetes.

## Table of Contents

- [Project Description and Goal](#Project Description and Goal)
- [Model Selection and Training](#Model Selection and Training)
- [Result Analysis](#Result Analysis)
- [Personal Reflection](#Personal Reflection)

## Project Description and Goal

This project focuses on diabetes, a chronic metabolic disease. Addressing the issue that traditional prediction methods—based on static factors such as age and gender—have limited accuracy, it aims to use the scikit-learn tool and various machine learning algorithms to build diabetes prediction models. The goal is to improve prediction accuracy and provide technical support for the early screening and intervention of diabetes. By analyzing a diabetes dataset containing 8 features (including the number of pregnancies, glucose levels, and blood pressure), the project compares the performance of different algorithms and ultimately selects high-quality models suitable for diabetes prediction.

## Model Selection and Training

Centering on the demand for diabetes binary classification prediction, this project selects 6 basic algorithms and 3 ensemble learning methods to construct models, including Logistic Regression, Random Forest, Decision Tree, SVC, as well as Bagging, AdaBoost, and GradientBoosting. At the data level, from the diabetes dataset (containing 8 features such as the number of pregnancies and glucose levels), the dataset is divided into training and test sets at a ratio of 78:22. A multi-dimensional indicator system is adopted to evaluate model performance, with core indicators including cross-validation scores, accuracy rates of the training and test sets, as well as precision, recall, and f1-score from the classification report.

![数据集分割图](/images/Split.png)

## Result Analysis

Logistic Regression showed stable performance, with a cross-validation score of 76.83%, a training set accuracy of 76.13%, and a test set accuracy of 81.66%. The three values are close, indicating no overfitting. For Random Forest, the training set accuracy reached 100%, but there was a significant gap between the cross-validation score (77.09%) and the test set accuracy (80.47%), posing a risk of overfitting. Decision Tree suffered from the most severe overfitting: while it achieved 100% accuracy on the training set, its accuracy on the test set was only 72.19%. Additionally, the classification report revealed that most models had low recall rates for the disease class (Outcome=1); for example, Logistic Regression had a recall rate of 61% for Class 1, which reflects that the models' ability to identify disease samples needs improvement.

From the overall results, Logistic Regression was the model with the best comprehensive performance. It balanced high test set accuracy (81.66%) and no overfitting, making it suitable for initial diabetes prediction scenarios. Among the ensemble methods, Bagging and AdaBoost had good generalization ability, while GradientBoosting (with a test set accuracy of 76.92%) delivered balanced and stable performance, so both could serve as alternative models. Although SVM achieved uniform scores across all datasets, it had relatively low overall accuracy and limited practicality. Due to severe overfitting, Decision Tree was difficult to apply in practical scenarios.

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

During this course project, I learned the core concepts and practical methods of machine learning techniques in the field of medical data analysis, including the application scenarios and parameter tuning of algorithms such as Logistic Regression and Random Forest, as well as how to align algorithm performance with actual medical needs. This project was a valuable technical growth experience for me, which strengthened my skills in the fields of machine learning and medical data processing.
