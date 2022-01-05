---
approaches: ["clustering"]
---
## Summary
Classify observations into $k$ categories, while minimizing distances within clusters and maximizing them between.

#### Steps
1. Initialize $k$ random centroids (e.g. points)
2. Assign each observation to closest centroidm, forming clusters
3. New centroids = mean coordinates of all assigned points in cluster
4. Repeat steps 2 + 3 until there are no more changes (good) or a certain number of iterations (bad)

## Notes
- $k$ needs to be provided
- *Outcome based on random seed*
- Hyperparameters
	- $k$: Number of catgories
	- Method of choosing first centroids
		1. Use random points
		2. Generate random values in feature space
	- Measure of (dis)similarity e.g. [[Concepts#Euclidean Distance|euclidean distance]]
- Evaluation
	- External: If there's a ground truth or other extra information, we can use that information to compare
	- Internal: Distances of data points within clusters as a measure of error
- How to choose $k$?
	- Higher $k$ => always lower error
	- Look for elbow, similar to PCA
- Pros
	- Can specify number of clusters
- Cons
	- Have to explicitly choose number of clusters
	- Can't detect outliers
