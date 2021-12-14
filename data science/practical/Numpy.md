## Numpy Arrays
Created via `x = np.array([...])`

- Number of dimensions: `x.ndim`, how deeply is the array nested / how many axes does it have? Corresponds to the number of indices needed to get actual values 
	- 1 corresponds to a classic array, list, column or row
	- 2 corresponds to a matrix, tabular data or a dataframe
- Shape: `x.shape` returns a tuple with a length corresponding equal to the number of dimensions
- **Axes, when more than one, 0 corresponds to rows and 1 corresponds to columns!**
- Data is accessed by indexing via e.g. `x[0]` , for two or more dimensional `x[0][0] = x[0,0]`, but stuff like `x[0, 0:2]` is also possible
- Multiplication
	- Standard multiplicationvia `*`  expects equal size (or a scalar) and multiplies each values with the other values at the same position (for scalar everything get's scaled by that number)
	- Matrix multiplication via `np.dot()`, this is the weird form of multiplciation; reduces shape and possible dimensionality!