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

## 目录

- [项目概述](#Project description and goal)
- [模型选择与训练](#Model Selection and Training)
- [结果分析](#Result Analysis)
- [个人反思](#Personal reflection)

## Project description and goal

本项目聚焦糖尿病这一慢性代谢疾病，针对传统基于年龄、性别等静态因素的预测方法准确率有限的问题，旨在借助 scikit-learn 工具，运用多种机器学习算法构建糖尿病预测模型，提升预测准确性，为糖尿病早期筛查与干预提供技术支持。项目通过分析包含怀孕次数、血糖、血压等 8 个特征的糖尿病数据集，对比不同算法性能，最终筛选出适用于糖尿病预测的优质模型。

## Model Selection and Training

本项目围绕糖尿病二分类预测需求，选择 6 种基础算法与 3 种集成学习方法构建模型，包括Logistic Regression、Random Forest、Decision Tree、SVC，以及 Bagging、AdaBoost、GradientBoosting。数据层面，从糖尿病数据集（含怀孕次数、血糖等 8 个特征）中，按 78:22 比例划分训练集与测试集。采用多维度指标评估模型性能，核心包括交叉验证得分、训练集与测试集的准确率，以及分类报告中的precision、recall、f1-score。

![](/images/diabetes-model-architecture.png)

## Result Analysis

逻辑回归表现稳定，交叉验证得分 76.83%、训练集准确率 76.13%、测试集准确率 81.66%，三者接近无过拟合；随机森林训练集准确率达 100%，但交叉验证（77.09%）与测试集（80.47%）得分差距明显，存在过拟合风险；决策树过拟合最严重，训练集 100% 准确率对应测试集仅 72.19%。此外，分类报告显示多数模型对疾病类（Outcome=1）召回率偏低，如逻辑回归 1 类召回率 61%，反映模型对患病样本的识别能力待提升。
从整体结果看，逻辑回归是综合性能最优的模型，兼顾高测试集准确率（81.66%）与无过拟合问题，适合糖尿病初步预测场景；集成方法中，Bagging 与 AdaBoost 泛化能力良好，GradientBoosting（测试集准确率 76.92%）性能均衡稳定，可作为备选模型；SVM 虽在各数据集上得分均匀，但整体准确率偏低，实用性较弱；决策树因严重过拟合，难以应用于实际场景。

![模型性能对比图](/images/diabetes-model-architecture.png)

## Personal reflection

在这个课程项目中，我学习了机器学习技术在医疗数据分析领域的核心概念与实践方法，包括逻辑回归、随机森林等算法的适用场景与参数调优以及如何将算法性能与医疗实际需求结合。这个项目对我来说是一次宝贵的技术成长经历，巩固了我在机器学习与医疗数据处理领域的技能。

![项目总结图](/images/diabetes-model-architecture.png)
