# ADC Document
- Main problem: Variable Selection
- LogReg

## Process
- 1. Data Quality Check
	- Exclude low variability variables
	- Exclude variables with too many NAs
	- Deal with outliers
- 2. Information Value Check
	- Use table of ref values for to interpret
	- Use binning of variables
- 3. Trend Check
	- Are there any counterintuitive trends (e.g. correlations) in the data?
	- Check for variables that are too highly correlated
	- Use LASSO
- 4 Performance Testing
	- Evaluate performance => Gini (among others)
