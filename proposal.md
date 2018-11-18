# Machine Learning Engineer Nanodegree
## Capstone Proposal
## What's Cooking?
Albert Pan  
September 3, 2018

## Proposal

### Domain Background

Food plays a major part in any culture around the world. In fact, the geographical characteristics and cultural associations of a region directly influence their cuisines. By investigating the ingredients used in various cuisines, we can gain a better understanding of the geographical and cultural landscape of different regions.

For this project, we can use machine learning techniques to attain useful predictions with our data. This project will give me an opportunity to work with real-world datasets and to learn about the relation between ingredients and cuisines. This kind of research can be expanded to other fields of study involving text classification.

### Problem Statement

Using the data provided by [Yummly](https://www.kaggle.com/c/whats-cooking-kernels-only/data), the challenge is to predict the cuisine of the dish from its list of ingredients. We can use a machine learning model that utilizes this data to predict the appropriate cuisine.

My strategy for solving this problem is as follows:
1. Download data from Kaggle
2. Explore data with visualizations
3. Preprocess data and extract features
4. Train and test model
5. Tune hyperparameters


### Datasets and Inputs

The dataset is composed of two JSON files. This [dataset](https://www.kaggle.com/c/whats-cooking-kernels-only/data) is made available from a Kaggle competition provided by Yummly.

The most important file is the `train.json` file, which has 39774 rows of data and contains three fields, `id`, `cuisine`, and `ingredients`. The `ingredients` field consists the list of ingredients for each dish, while our target variable `cuisine` denotes the cuisine. The `id` field is a unique integer identifier for that particular dish. The `test.json` file has all the fields mentioned in the `train.json` file with the exception of our target variable, `cuisine`, and it has 9944 rows of data. In particular, I will be using the `ingredients` field as my features that I will pass into my model to train and predict the cuisine of the dish represented by the list of ingredients. Once I obtain the predictions of the data points in `test.json`, I will couple the `id` of the dish alongside with its respective prediction and submit it for the Kaggle [What's Cooking](https://www.kaggle.com/c/whats-cooking-kernels-only) competition.

### Solution Statement

Dishes of the same cuisine will likely share a common set of ingredients. I will be taking a look at the most frequent ingredients used for each cuisine, and use the individual ingredients as input features for the model I will be training.

I will begin by using a variety of classification models that we have learned throughout the course, such as SVMs, Decision Trees, Random Forest, etc., as well as the XGBoost model and possibly deep learning models. I will additionally explore the viability of clustering algorithms and see if dishes of the same cuisine cluster together.

### Benchmark Model
_(approximately 1-2 paragraphs)_

In this section, provide the details for a benchmark model or result that relates to the domain, problem statement, and intended solution. Ideally, the benchmark model or result contextualizes existing methods or known information in the domain and problem given, which could then be objectively compared to the solution. Describe how the benchmark model or result is measurable (can be measured by some metric and clearly observed) with thorough detail.

### Evaluation Metrics
_(approx. 1-2 paragraphs)_

In this section, propose at least one evaluation metric that can be used to quantify the performance of both the benchmark model and the solution model. The evaluation metric(s) you propose should be appropriate given the context of the data, the problem statement, and the intended solution. Describe how the evaluation metric(s) are derived and provide an example of their mathematical representations (if applicable). Complex evaluation metrics should be clearly defined and quantifiable (can be expressed in mathematical or logical terms).

### Project Design
_(approx. 1 page)_

In this final section, summarize a theoretical workflow for approaching a solution given the problem. Provide thorough discussion for what strategies you may consider employing, what analysis of the data might be required before being used, or which algorithms will be considered for your implementation. The workflow and discussion that you provide should align with the qualities of the previous sections. Additionally, you are encouraged to include small visualizations, pseudocode, or diagrams to aid in describing the project design, but it is not required. The discussion should clearly outline your intended workflow of the capstone project.
