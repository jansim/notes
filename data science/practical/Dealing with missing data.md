# Dealing with missing data

### Options
- check with collection source - can we maybe still find the data?
- Drop the missing data
	- exclude either column or rows
	- Python: `df.dropna()`
		- `dropna(subset=[...]` which columns to look at
		- `dropna(axis=0)` drop rows
		- `dropna(axis=1)` drop columns
	- R
		- `na.omit()` drop rows
		- `df[ , colSums(is.na(df)) == 0]` drop columns
- relace missing data => impute data
	- replace with average or similar data
	- replace based on extra knowledge
	- Python
		- `df['colname'].replace(np.nan, NEW_VAL)`
	- R/tidyverse
		- `replace_na(colname, NEW_VAL)`
- Can also leave as missing / NA