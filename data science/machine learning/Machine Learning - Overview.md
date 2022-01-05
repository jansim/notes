4 main approaches / problems
- Classification
- Regression
- Clustering
- Recommendation

# Approaches
Machine learning approaches / problems are typically categorized into four distinct categories (with some minor overlaps).

These four categories are:
1. Regression
2. Classification
3. Clustering
4. Recommendation

## Regression
Trying to predict a continuous / numerical outcome e.g. profit, temperature.

## Classification
Trying to predict a discrete category or the probabilty of a belongig to a category e.g. risk of defaulting on a credit card.

- Can be applied to regression problems, if it's ok to bin them (e.g. two categories of <= 50 and > 50)

## Clustering
Identify clusters in the data and assign observations to them. This a form of [[Concepts#Unsupervised Supervised Machine Learning|unsupervised learning]].

  - Can also be used for recommendation

## Recommendation
Provide suggestions / recommendations of what someone might like based on their past interactions. There are two leading approaches within recommendation: collaborative filtering (👱) and content-based (📋️) filtering.
- Often also referred to as *Recommender Systems*.
- 2 main approaches
  - **Collaborative Filtering**: Based on other users w/ similar interests i.e. recommend music similar people also listened to
  - **Content-based Filtering**: Based on properties of the thing itself i.e. recommend music w/ similar properties
- Implementation
   - Memory based
	   - All data in memory
   - Model based
	   - Create an actual model with a set of parameters, but not retaining the whole dataset in the model

# Algorithms
- Classic
	- [[Linear Regression]]:
	- [[Logistic Regression]]: Kind of like linear regression, but for the log() of the odds of an event happening.
- [[k-Nearest Neighbours (kNN)]]: Find the k most similar observations and use their mean.
- [[Linear Discriminant Analysis (LDA)]]: Flips problem on its head: Models the distribution of predictors for each level of outcome and then uses bayes theorem to determine the most likely class for the given data.
- [[Quadratic Discriminant Analysis (QDA)]]: Like LDA, but does not assume equal variance of features.
- [[LASSO & Ridge Regression]] (Regularized Regression): Similiar to normal regression models (linear / logistic), but shrinking coefficients with a penalty.
- Tree Based
	- [[Random Forest]]: Construct many (i.e. hundreds / thousands) of decision trees and use the average / most common prediction of them.
	- [[Decision Trees]]: Find optimal splits based on features and construct a tree of choices.
- [[Support Vector Machine (SVM)]]: Find a plane (in n-fold feature space) to separate observations. Supports different kernels.
- Neural Networks / Deep Learning
	- Neural Networks
	- Reinforcement Learning
	- Convolutional Neural Networks
	- Shallow Neural Networks
	- Transformers
- Types of Fitting
	- Bagging: Bootsrap aggregation => fit on multiple bootstrapped datasets (from your original single dataset) and use the average / most common prediction.
	- Boosting: Similar to bagging, but sequential i.e. each addition improves performance as it is fitted on residuals
- Clustering
  - k-Means: Needs a prespecified number of clusters k
  - Hierarchical Clustering: generates a tree, which we can chop off somewhere to get nested clusters
  - DBSCAN (Density Based Clustering of Applications with Noise): Density based, can do arbitrary shapes, can detect outliers
    - **R**adius 
    - **M**inimum number of Neighbours
