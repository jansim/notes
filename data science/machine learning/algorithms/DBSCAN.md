---
approaches: ["clustering"]
---
## Summary

### Steps
1. Examine all points and assign them a category
	- *core point* if $\geq m$ points within a distance of $r$
	- *border point* if $< m$ points within a distance of $r$, but one of them is a core point
	- else *outlier*
2. Create clusters by assigning all groups of connected core and border points into single clusters

## Notes
- **D**ensity-**b**ased **s**patial **c**lustering of **a**pplications with **n**oise
- Allows for arbtriary shaped clusters and clusters within clusters
	- Think of a 🔴 in a 🍩
- Pros
	- Flexible shapes
	- Has a concept of outliers (and is thus robust to them)
	- No need to specify number of clusters
- Cons
- Hyperparameters
	- $r$: Radius 
    - $m$: Minimum number of Neighbours
