## Formulas
$Precision = \frac{true_{pos}}{all_{pos}} = \frac{true_{pos}}{true_{pos} + false_{pos}}$

$Accuracy = \frac{all_{true}}{all} = \frac{true_{pos} + true_{neg}}{N}$

Sensitivity, Recall, True Positive Rate: $Sensitivity = \frac{true_{pos}}{all that should be pos} = \frac{true_{pos}}{true_{pos} + false_{neg}}$

Specificity, True Negative Rate: $Specificity = \frac{true_{neg}}{all that should be neg} = \frac{true_{neg}}{true_{neg} + false_{pos}}$

F-Score: Harmonic Mean (mean for rates) of Precision and Sensitivity. $F_1 = \frac{2}{Sensitivity^{-1} * Precision^{-1}} = \frac{true_{pos}}{true_{pos} + 0.5(false_{pos} + false_{neg})}$

## Recommender Systems
- **Collaborative Filtering**: Based on other users w/ similar interests i.e. recommend music similar people also listened to
- **Content-based Filtering**: Based on properties of the thing itself i.e. recommend music w/ similar properties

## Typical Questions

### How to deal with missing data
It depends:
- If high N we might be able to just drop the observations
- If the setting permits it, we might be able to impute missing observations. (Could also just be set to 0 if it makes sense)

## Concepts
- **Law of Large Numbers**: Back-bone of freq. statistics; 
- **Selection Bias**: Error due to non-random sample from population
- **Survivorship Bias**: Non-random dropout leading to weird sample.

- **One-hot encoding / Dummy coding**: Turn categorical variables into numerical ones.

## Models
- SVM
- Random Forest
- Decision Tree
- LDA
- QDA
- Logistic Regression
- Linear Regression


ToDo:
eigenvalue; eigenvector

## To Learn
- gaussian mixture models
- 