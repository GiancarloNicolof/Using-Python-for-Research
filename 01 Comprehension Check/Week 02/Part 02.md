# Part 02: NumPy

- **True or False: a `numpy` array's length may be modified after being created.**
    > False

- **Consider the following object: `numpy.array([0., 0., 0., 0., 0.])`. What code will produce that object?**
    > `numpy.zeros(5)`

- **Consider the following code:**
    ```python
    x = numpy.array([[3,6], [5,7]])
    y = x.transpose()
    print(y)
    ```
    What does this print?
    > `array([[3 5], [6 7]])`

- **Consider the following code:**
    ```python
    x = np.array([1,2,5])
    x[1:2]
    ```
    What does this return?
    > `array([2])`

- **Consider the following code:**
    ```python
    a = np.array([1,2])
    b = no.array([3,4,5])
    a + b
    ```
    What does this return?
    > This code contains an error.

- **Consider the following code:**
    ```python
    a = np.array([1,2])
    b = np.array([3,4,5])
    b[a]
    ```
    What does this return?
    > `array([4,5])`

- **Consider again the above code, as well as the following:**
    ```python
    c = b[1:]
    b[a] is c
    ```
    What does Python return?
    > False

- **Consider the following code:**
    ```python
    x = 20
    not np.any([x%i == 0 for i in range (2, x)])
    ```
    What does the above code do?
    > Finds whether `x` is prime.