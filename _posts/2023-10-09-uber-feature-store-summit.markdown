---
title: "Feature Store Summit"
layout: post
date: 2023-10-09 00:00
image: /assets/images/2023-07-01-llama-love/teampic.jpg
headerImage: false
tag:
- AI
- Data Engineering
- Software Engineering
- Machine Learning
category: project
projects: true
author: chrissettles
description: Presenting at Hopswork's Feature Store Summit
---
# Experience presenting at Hopswork's Feature Store Summit

![Screenshot from recording of talk, current slide presnted demonstrates some storage optimizations for creating a write log.](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/changelog.jpeg)

I was invited to be a [speaker](https://www.featurestoresummit.com/fss-2023/speakers) at [Hopswork's](hopsworks.ai) feature store summit. For many companies, feature stores are the primary source of information when providing intelligent decisions. Uber is no different. As a machine learning engineer on Uber's risk team, I felt it appropriate for us to present some of the helpful ML Infrastructure our teams have worked on to enable our advanced risk platform which we have named the "Knowledge platform". For Uber's Risk team, this was a big opportunity since it would be the first time our Risk Infrastructure would be presented publicly since 2018 (Pre-IPO)

Over the years I've gotten to become familiar with the pattern for ML for fraud usecases. Most of the problems we deal with would lie in the realm of binary classification, in either the supervised or unsupervised realm. For a company as big as uber and only a small set of machine learning engineers, the most important problem to solve is to quickly set up a model's training data, train a simple model (i.e. XGBoost or otherwise), appropriately evaluate the model on various validation sets (see [out-of-time sampling](https://docs.datarobot.com/en/docs/modeling/special-workflows/otv.html) and [out-of-sample sampling](https://stackoverflow.com/questions/5087635/out-of-sample-definition)). 

This simplicity in the solution makes the role of an elaborate and effective feature computation platform all the more important for providing business value. Many time-sink problems that come up today are along the line of organizing the data in the offline data warehouse (HDFS, Hive, etc...) so that point-in-time-correct joins can be done efficiently by machine learning engineers at the time they wish to train a new model with a new set of features. 

Given that our machine learning for fraud relies heavily on this ecosystem for delivering features to models for both training and serving, I was delighted when both Jean Cai and Kaavya Srinivasan [agreed to co-present](https://www.featurestoresummit.com/session/ubers-risk-knowledge-platform) with me to share more in-depth details about Uber's uGraph feature computation platform and uFlow feature store. 

Overall, the team at Hopsworks was very organized in setting timelines, flexible to allow us to add speakers, and understanding of how we wanted to showcase our work. We were glad to have filled the time with enough content about our Infrastructure configurations, optimizations, and our tools for ML Training data creation. 

If you are interested, can view the slides for our talk [here](https://content.hopsworks.ai/hubfs/Feature%20Store%20Summit%202023/FS%20Summit%2023%20-%20Uber%20(Risk%20Platform).pdf) and the recording [here](https://www.youtube.com/watch?v=KZe1dFjK1dY&ab_channel=FeatureStoreOrg). You can view all the recordings for other speakers at the conference [here](https://www.featurestore.org/feature-store-summit-2023?utm_source=fs-summit&utm_medium=web)
