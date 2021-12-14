Finding the optimal values for different tuning parameters of a given method. Typically done by performing a grid-search of parameters combinations alongside cross validation to evaluate fit.


- Python/Scikit-learn
	- `sklearn.model_selection.GridSearchCV`
	- `result = GridSearchCV(modelInstance, listofParameterDicts, cv = 5).fit(x, y)`
	- Outcome: result.best_estimator_ and result.cv_results_
- R/caret
	- 