---
approaches: ["clustering"]
---
## Summary
Generates a tree of clusters, which we can chop off at some point to get a nested list of clusters.

### Steps (Agglomerative / bottom-up)
1. Treat each observation as its own mini-cluster
2. Calculate distances between all (mini) clusters
3. Assign the two *closest* observations / clusters to a slightly larger cluster
4. Repeat Step 2 & 3 until there is only one cluster left
5. You now have a very detailed tree, which can be cut off anywhere to get an exact number of $X$ clusters

## Notes
- 🌳 Two approaches
	- ⏬ Divisive (top-down)
	- ⏫ Agglomaretive (bottom-up)
- Have to choose where to cut off tree
- Hyperparameters / Choices
	- Linkage / How to compute distance when there are multiple points
		- Single-Linkage Clustering: Minimum distance of closest points between two clusters
		- Complete-Linkage Clustering: Maximum distance of furthest points between two clusters
		- Average Linkage Clustering: Average distance between all points in two clusters
		- Centroid Linkage Clustering: Distance between cluster centroids
- Pros
	- Produces a whole tree of clusters
	- No need to specify number of clusters ahead of time
- Cons
	- Can be slow
	- Have to choose where to cut off tree
