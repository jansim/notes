---
approaches: ["regression"]
---
## Summary
Create an optimal, weighted linear combination of predictors. Can only predict linear trends, still widely used esp. the [[Logistic Regression|logistic]] variant.

### Formula
$y = b_1*x_1 + b_2*x_2 + ... + b_n$
- $y$: outcome
- $x_n$: predictor n
- $b_{n}$: weight for predictor n
- $b_n$: Intercept

## Notes
- Very classic form of ML
- Easily interpretable, not that flexible
- Optimized using Least Squares
- Categorical variables are encoded using [[Concepts#One-hot encoding Dummy coding]].
- Hyperparameters
	- Intercept or not
