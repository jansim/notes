# EDA
Convention: predictor on x axis, outcome on y axis

## Descriptive Statistics
- Python:
	- For continuous data `df.describe()`
	- For categorical data: `df[...].value_counts()`
- R: `skimr::skim(df)`
	- Tip: `as.data.frame(skimr::skim(df))` returns a data frame that can also be `View`-ed in Rstudio

## Plot
### Scatterplots
x: continuous; y: continuous

- Python: `sns.scatterplot(x="col", y="col", data=df)`
	- `plt.scatter(df['x'], df['y'])`, still have to do labeling etc!
- R: `ggplot(df, aes(x = col, y = col)) + geom_point()`

### Boxplots
x: categorical; y: continuous

- Python: `sns.boxplot(x="col", y="col", data=df)`
- R: `ggplot(df, aes(x = col, y = col)) + geom_boxplot()`

### Regression

- Python: `sns.regplot()`
- R: `geom_smooth(method='lm')`