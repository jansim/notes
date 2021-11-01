## Based upon Confusion Matrix

##### Precision
Fraction of predicted positive cases that is actually actually truly positive.

$Precision = \frac{true_{pos}}{all_{pos}} = \frac{true_{pos}}{true_{pos} + false_{pos}}$

##### Accuracy
Fraction of correctly identified cases overall.

$Accuracy = \frac{all_{true}}{all} = \frac{true_{pos} + true_{neg}}{N}$

##### Sensitivity
Fraction of all true positive cases that have been correctly identified by the model.

Other names: Sensitivity, Recall, True Positive Rate

$Sensitivity = \frac{true_{pos}}{all that should be pos} = \frac{true_{pos}}{true_{pos} + false_{neg}}$

##### Specificity
Fraction of (all) negative cases that has been correctly identified.

Other names: Specificity, True Negative Rate

$Specificity = \frac{true_{neg}}{all that should be neg} = \frac{true_{neg}}{true_{neg} + false_{pos}}$

##### F-Score
F-Score: Harmonic Mean (mean for rates) of Precision and Sensitivity.

$F_1 = \frac{2}{Sensitivity^{-1} * Precision^{-1}} = \frac{true_{pos}}{true_{pos} + 0.5(false_{pos} + false_{neg})}$

## ROC & Derivatives

##### ROC: Receiver Operating Characteristic curve
Shows detection of positives / negatives in a binary classifier when varying the threshold of decision.

Random classifier => diagonal; Perfect classifier top left corner.

- Left axis: true positive rate
	- fraction of (all) positive cases that has been correctly detected
- Bottom axis: false positive rate
	- fraction of (all) negative cases that has been incorrectly predicted as positive

##### AUC: Area Under Curve (talking about ROC)
The area under the ROC curve.

Ranges from 0 to 1 random with random classifier at a value of 0.5.

Other names: c-statistic.

##### Gini Coefficient
Based on AUC (with other possible formulas).

$Gini = (2 * AUC) - 1$

Ranging from -1 to 1,  while 0 corresponds to chance. -1 would be perfect misclassification.
