---
approaches: ["classification", "regression"]
---
## Summary
Construct many (i.e. hundreds / thousands) of decision trees and use the average / most common prediction of them. When constructing the trees each one of them only has access to a subset of variables $m$ and is fitted on a bootsrapped sample of the data.

## Notes
- Surprisingly good real world performance.
- Hyperparameters
	- Number of trees
	- Number of variables to provide $m$
		- Often: $m = \sqrt{p}$ with $p =$ all predictiors