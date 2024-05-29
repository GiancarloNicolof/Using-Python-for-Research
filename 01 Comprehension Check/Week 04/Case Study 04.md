# Case Study 04: Classifying Whiskies

- **What is Pandas?**
	> A Python library designed to query and manipulate annotated data tables.

- **What keyword allows you to specify names to indices in a `pd.Series`?**
	> `index`

- **In `pandas`, what does the `reindex` method do?**
	> Reorders the indices of a `pandas` Series object according to its arguments.

- **What command reads in `csv` files in `pandas`?**
	> `pd.read_csv`

- **How can you find a correlation matrix of a `pd.Dataframe`?**
	> `pd.DataFrame.corr`

- **How can you plot a correlation matrix by color?**
	> `plt.pcolor`

- **What is the `matplotlib.pyplot` function that plots a colorbar on the side of a plot?**
	> `plt.colorbar()`

- **What is spectral co-clustering?**
	> A method for finding clusters of objects by the similarity of their attributes.

- **How many clusters do we find in the whisky dataset in Video 4.1.4?**
	> 6

- **Consider the following code:**
	```python
	import pandas as pd
	data = pd.Series([1,2,3,4])
	data = data.ix[[3,0,1,2]]
	```
	What does `data[0]` return? Why?
	> `1`: `data.ix` reorders the order of appearance, but leaves the indices the same.

- **Consider the following code:**
	```python
	import pandas as pd
	data = pd.Series([1,2,3,4])
	data = data.ix[[3,0,1,2]]
	data = data.reset_index(drop = True)
	```
	What does `data[0]` return? Why?
	> `4`: The 0th index of the data has been reordered to index 3 of the original, which is 4.