## Scaling
Some modeling techniques such as linear regression are affected by a variables scale e.g. a variable in the thousands will be treated as more impactful than a variable in the tens.
To adjust for this fact, variables can be rescaled into a similar scale.

- Options
	- can divide by column maximum
	- z-scoring
		- Python: `sklearn.preprocessing.StandardScaler`
		- R: scale()

## Binning
To deal with outliers or for easier interpretation in e.g. logistic regression.

- Python
	- `bins = np.linspace(min(df['col']), max(df['col']), N_BINS)`
	- `df['binned'] = pd.cut(df['col'], bins, labels = [...], include_lowest=T)`

## One-Hot-Encoding
- Python
	- 

## Feature Engineering

### Polynomials
- np.polyfit()