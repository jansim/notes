### Pipeline Steps
- `step = StepConstructor()`
	- step.fit() to get proper values
	- step.transform() to apply to data
	- step.predict() to predict new data
- `pipe = Pipeline([('name', step), ...])`
	- pipe also has fit and predict

### Preprocessing
`sklearn.preprocessing`
- Can create many different steps

- Scaling: `StandardScaler`

### Model Fitting