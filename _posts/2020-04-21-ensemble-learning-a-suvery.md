---
layout: default
title: "Ensemble learning: Review and summary"
date: 2020-04-21 13:00:00 +0200
published: 2020-04-21 13:00:00 +0200
comments: false
categories: development
tags: [Machine learning, Ensemble learning]
github: "https://github.com/JIWANG176"
---
Ensemble methods are considered the state-of-the art solution for many machine learning challenges. Such methods improve the predictive performance of a single model by training multiple models and combining their predictions. Based on **Ensemble learning: A survey (Omer Sagi, Lior Rokach, 2017)**, I summarize the concept and challengs of ensembel learning nowadays and provide a through review of subjects that currently unter intense study.
<!--more-->

&nbsp;
## Introduction
Ensemble learning is an umbrella term for methods that combine multiple inducers to make a decision, typically in supervised machine learning tasks. An inducer, also referred as a base-learner, is an algorithm that takes a set of labeled examples as input and produces a model (e.g., a classifier or regressor) that generalizes these examples. By using the produced model, predictions can be drawn for new unlabeled examples. An ensemble inducer can be of any type of machine learning algorithm (e.g., decision tree, neural network, linear regression model, etc.). **The main premise of ensemble learning is that by combining multiple models, the errors of a single inducer will likely be compensated by other inducers, and as a result, the overall prediction performance of the ensemble would be better than that of a single inducer.**





&nbsp;
## Ensemble learning foundations
Ensemble learning refers to the generation and combination of multiple inducers to solve a particular machine learning task. The intuitive explanation for the ensemble methodology stems from human nature and the tendency to gather different opinions and weigh and combine them to make a complex decision. The main idea is that weighing and aggregating several individual opinions will be better than choosing the opinion of one individual. 

### Why ensemble methods work?
There are several reasons why ensemble methods often **improve predictive performance** (Dietterich, 2002; Polikar, 2006):

- **Overfitting avoidance**: When just a small amount of data is available, a learning algorithm is prone to finding many different hypothesis that predict all of the training data perfectly while making poor predictions for unseen instances. Averaging different hypothesis reduces the risk of choosing an incorrect hypothesis and therefore, improves the overall predictive performance.

- **Computational advantage**: Single learners that conduct local searches may get stuck in local optima. By combining several learners, ensemble methods decrease the risk of obtaining a local minimum.

- **Representation**: The optimal hypothesis may be outside the space of any single model. By combining different models, the search space may be extended and hence, a better fit to the data space is achieved.

### Ensemble learning and unique machine learning challenges
There are several settings that pose nontrivial challenges to machine learning algorithms. Ensemble methods may be used to mitigate these challenges as described below:
- **Class imbalance**:
    - Using a balanced subsample of the data (Nikulin & Ng, 2009).
    - Combining random under-sampling techniques with ensemble techniques such as bagging or boosting (Galar, Fernandez, Barrenechea, Bustince, & Herrera, 2012).
    - Using the EUSBoost method which leverages evolutionary under-sampling to promote diversity among individual inducers (Galar, Fernández, Barrenechea, & Herrera, 2013).

- **Concept drift** (for real-time machine learning applications):
    - Using dynamic weighted majority (DWM) method, in which individual decision trees are dynamically created and deleted according to changes in predictive performance (Kolter & Maloof, 2003).
    - Different diversity levels of ensembles (Minku, White, & Yao, 2010; Minku & Yao, 2012).
    - ADWIN is another approach in which ensemble members can be reset when their accuracy degrades significantly (Bifet, Frank, Holmes, & Pfahringer, 2010). This method may also be integrated with online bagging ensembles (Bifet, Holmes, Pfahringer, Kirkby, & Gavaldà, 2009).

- **Curse of dimensionality**:
    - Attribute bagging (AB), an approach in which an inducer is trained using a randomly selected subset of features (Bryll, Gutierrez-Osuna, and Quek, 2003).
    - Improved decision forest (IDF) which addresses high-dimensional datasets by applying a designated feature selection mechanism (Huang, Fang, & Fan, 2010).
    - A genetic algorithm that searches for the best mutually exclusive partition of the feature set, insted of the random partition (Rokach, 2008).
    - The optimal feature set partitioning (OFSP) method, which creates a fixed number of feature views in advanced towards reducing dimensionality and optimizing accuracy (Kumar & Minz, 2016).






&nbsp;
## Building an ensemble model
Given a dataset of $n$ examples and $m$ features $D = {(xi, yi)} (|D| = n, x_i/in R^m, y_i/in R)$, an ensemble learning model $φ$ uses an aggregation function $G$ that aggregates $K$ inducers, ${f_1, f_2, /dots, f_k}$ towards predicting a single output as follows:

$$y_i = φ(xi) = G(f_1, f_2, /dots, f_k)$$

where $y_i/in R$ for regression problems and $y_i/in Z$ for classification problems. Given this general framework, building an ensemble model involves the selection of a methodology for training the participating models and choosing a suitable process for combining the inducers' outputs.

### Model training
There are several ways to train an ensemble model to reach a desired outcome. However, **some key principles** must be considered when generating an ensemble model:
- **Diversity**
- **Predicitive performance**

The two principles may seem to contradict each other at first glance. Furthermore, ensembles with diverse inducers do not always improve the predictive performance (Bi, 2012). The main idea in combining these two principles is to combine predictive inducers with uncorrelated errors in an ensemble, since it has been empirically and theoretically shown that the predictive performance of the entire ensemble has a positive correlation with the degree to which the errors made by individual inducers are uncorrelated (Ali & Pazzani, 1995). 

There are **several approaches used to achieve the goal of including diverse inducers**:
- *Input manipulation*
- *Manipulated learning algorithm*
- *Partitioning*
- *Output manipulation*
- *Ensemble hybridization*

### Output fusion
Output fusion refers to the process of integrating the base model outputs into a single output. The following section summarizes the main approaches for combining the outputs:
- *Weighting methods*
- *Meta-learning methods*





&nbsp;
## Ensemble methods
More will be updated in the feature..


&nbsp;
