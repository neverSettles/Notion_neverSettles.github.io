---
title: "Binary Classification Metrics"
layout: post
date: 2023-12-16 00:00
image: /assets/images/2023-12-16-bin-metrics/metrics.jpg
headerImage: false
tag:
- binary classification
- metrics
- machine learning
category: blog
author: chrissettles
description: Understanding the relationships between various metrics in binary classification.
---

# Binary Classification Metrics

It's magical how many metrics exist to evaluate a problem that outputs only two possibilities - 0 or 1. Here we will derive a formulated way of understanding the relationships between all these methods of evaluation.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/55a836b8-a5fc-4640-a464-f4a6944f0ec4/Untitled.png)

Reviewing the confusion matrix, we see that supervised binary classification leads to one of four possible outcomes: 

True Negative, False Positive
False Negative, True Positive

Summing the matrix horizontally, we get the **actual** number of negative and positive examples:

Actual Negative = TN + FP
Actual Positive = FN + TP


Summing vertically, we get the **predicted** number of negative and positive examples:

Predicted Negative = TN + FN
Predicted Positive = TP + FP


There are a few different binary classification metrics we can use to assess the quality of the predicted outcomes. 

A 3-dimensional question we can use to derive any of the metrics is:

<aside>
💡 **When x y, how often is it z?**
</aside>

Then, the 3 dimensions of a binary classification metric are:

1. x - the actual label is / the model predicts
2. y - 1 / 0
3. z - Correct / Incorrect

From these 3 different dimensions, we can derive 8 different metrics for evaluating a binary classification problem.

The first 4 metrics focus on the correct predictions - the numerator focuses on what the model got right (the True Positives and True Negatives):

1: **True Positive Rate (TPR) / Recall / Sensitivity** - When the actual label is 1, how often are we correct?

= TP / (TP + FN)
= TP / Actual Positive
= 1 - FN / (TP + FN)
= 1 - FNR


2: **Precision** - When the model predicts 1, how often are we correct?

= TP / (TP + FP)
= TP / Predicted Positive
= 1 - FP / (TP + FP)


3: **True Negative Rate (TNR) / Specificity** - When the actual label is 0, how often are we correct?

= TN / (TN + FP)
= TN / Actual Negative
= 1 - FP / (TN + FP)
= 1 - FPR


4: **Unnamed** - When the model predicts 0, how often are we correct?

= TN / (TN + FN)
= TN / Predicted Negative
= 1 - FN / (TN + FN)


The next 4 metrics focus on the incorrect predictions - the numerator focuses on what the model got wrong (the False Negatives and False Positives):

5: **False Negative Rate (FNR)** - When the actual label is 1, how often are we incorrect?

= FN / (TP + FN)
= FN / Actual Positive
= 1 - TPR


6: **Unnamed** - When the model predicts 1, how often are we incorrect?

= FP / (TP + FP)
= FN / Predicted Positive
= 1 - TP / (TP + FP)


7: **False Positive Rate (FPR)** - When the actual label is 0, how often are we incorrect?

= FN / (TN + FP)
= FN / Actual Negative
= 1 - TNR


8: **Unnamed** - When the model predicts 0, how often are we incorrect?

= FN / (TN + FN)
= FN / Predicted Negative
= 1- TN / (TN + FN)


And there we have it, the 8 key metrics fundamental for evaluating a binary classification problem fixing a threshold. However, note that more metrics exist that help combine these foundational metrics to evaluate a model across multiple thresholds (F1 score, AUC for ROC curve, AUC for Precision Recall curve, etc…).

I hope this post gave you a better foundation for understanding the relationships between the different metrics for evaluating binary classification problems.

---
