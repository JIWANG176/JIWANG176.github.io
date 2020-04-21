---
layout: default
title: "Ensemble learning: A suvery"
date: 2020-04-21 13:00:00 +0200
published: 2020-04-21 13:00:00 +0200
comments: false
categories: development
tags: [Machine learning, Ensemble learning]
github: "https://github.com/JIWANG176"
---
Ensemble methods are considered the state-of-the art solution
for many machine learning challenges. Such methods improve the 
predictive performance of a single model by training multiple models 
and combining their predictions. This paper introduce the concept of 
ensemble learning, reviews traditional, novel and state-ofthe-art 
ensemble methods and discusses current challenges and trends in the field.
<!--more-->

&nbsp;
## Introduction
Ensemble learning is an umbrella term for methods that combine multiple inducers to make a decision, typically in supervised machine learning tasks. An inducer, also referred as a base-learner, is an algorithm that takes a set of labeled examples as input and produces a model (e.g., a classifier or regressor) that generalizes these examples. By using the produced model, predictions can be drawn for new unlabeled examples. An ensemble inducer can be of any type of machine learning algorithm (e.g., decision tree, neural network, linear regression model, etc.). The main premise of ensemble learning is that by combining multiple models, the errors of a single inducer will likely be compensated by other inducers, and as a result, the
overall prediction performance of the ensemble would be better than that of a single inducer.

&nbsp;
## Ensemble learning foundations
Ensemble learning refers to the generation and combination of multiple inducers to solve a particular machine learning task. The intuitive explanation for the ensemble methodology stems from human nature and the tendency to gather different opinions and weigh and combine them to make a complex decision. The main idea is that weighing and aggregating several individual
opinions will be better than choosing the opinion of one individual. An example for such a decision is matching a medical treatment to a disease (Polikar, 2006).

### Why ensemble methods work?
- Overfitting avoidance
- Computational advantage
- Representation

### Ensemble learning and unique machine learning challenges
- Class imbalance
- Concept drift
- Curse of dimensionality

&nbsp;
## Building an ensemble model
More will be updated in the feature..
&nbsp;
&nbsp;