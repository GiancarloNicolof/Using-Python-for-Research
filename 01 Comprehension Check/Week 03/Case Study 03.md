# Case study 03: Introduction to Classification

- **How does the *k* -Nearest Neighbors classifier classify observations?**
	> According to the most common class among the nearest *k* neighnbors.

- **How is the distance measure we use (Video 3.3.2) defined between the points `(a1, b1)` and `(a2, b2)`?**
	> $\sqrt{ (a_{1} - a_{2})^2 + (b_{1}-b_{2}) }$

- **What does the `items` method for dictionaries return?**
	> A `dict_items` object with elements consisting of tuples of key, value pairs.

- **What will `random.choice()` return for a list containing only one object? (Assume that the `random` module has already been imported.)**
	> This code returns the single element every time.

- **For an `np.array` of dimension 2, what does the `shape` method return?**
	> A tuple containing the number of rows and columns

- **What does `np.argsort` do?**
	> It sorts an array according to a single argument and returns the sorted indices. 

- **What does `np.concatenate` do?**
	> Takes in a tuple of `np.arrays` and joins them lengthwise along the specified axis.

- **What is the main benefit of generating synthetic data?**
	> You know exactly how the data were generated so you know what to expect when testing code.

- **What does `np.arange` do?**
	> Creates regularly spaced values between the first and second argument, with spacing given in the third argument.

- **What does `enumerate` do?**
	> Takes an iterable and returns a new iterable with tuples as elements, where the first index of each tuple is the index of the tuple in the iterable.

- **What are the four variables in the `iris` dataset described in Video 3.3.8?**
	> Sepal length, sepal width, petal length, petal width

- **How many different species are contained in the `iris` dataset described in Video 3.3.8?**
	> 3

- **How often do the predictions from the homemade and `scikit-learn` kNN classifiers accurately predict the class of the data in the `iris` dataset described in Video 3.3.8?**
	> Approximately 85% of the time.