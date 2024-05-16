# Part 04: Randomness and Time

- **Use `random.choice` and `range` to generate a random integer from 0-9.**
    > `random.choice(range(0,10))`

- **What will `random.choice(list([1, 2, 3, 4]))` produce?**
    > A value from 1 to 4, selected at random.

- **Which of the following lines of code takes the sum of 10 random integers between 0 and 9?**
    > `sum(random.choice(range(10)) for i in range(10))`

- **What will `random.choice(list((1,2,3,4)))` do?**
    > Sample from the list `[1,2,3,4]`

- **What is the law of large numbers with respect to histograms?**
    > We expect the histogram of a sample to better reflect the distribution as the sample size increases.

- **What is the Central Litim Theorem?**
    > The distribution of the sum of many random variables is approximately normal.

- **What does `numpy.random.random((5,2,3))` do?**
    > Generates a 5 x 2 x 3 NumPy array with random uniform values.

- **What does `numpy.random.normal(1,2,3)` do?**
    > Generates 3 samples with mean 1 and standard deviation 2.

- **What does `numpy.random.randint(1,5,(2,3))` do?**
    > Generates a 2 x 3 array with random integers from `1.4`.

- **What is the dimension of `numpy.sum(numpy.random.randint(1,7,(100,10)), axis=0)`?**
    > 10.

- **Consider the following code:**
    ```python
    start_time = time.clock()
    stop_time = time.clock()
    stop_time - start_time
    ```
    What does this return?
    > A `float` of the seconds between the two times.

- **How are the displacements, the individual steps, in the random walk related to one another?**
    > Any two consecutive displacements are independent of one another.

- **What does `np.concatenate` do?**
    > Takes an iterable of `np.arrays` as arguments, and binds them along the `axis` argument.