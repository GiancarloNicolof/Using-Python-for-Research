# Part 03: Manipulating Objects

- **Consider the following code: `x=3`. `x` did not exist in memory prior to this code. Which of the following does NOT occur?**
    
    > The object `3` refers to the variable name `x`.
    

- **Consider the following code:**

    ```python
    x=3
    y=x
    y=y-1
    ```
    **What does `x` equal?**
    
    > 3
    

- **Consider the following code:**

    ```python
    L1 = [2,3,4]
    L2 = L1
    L2[0] = 24
    ```
    **What does `L1` equal?**
    
    > `[24, 3, 4]`
    

- **Consider the following code:**

    ```python
    L = [2,3,4]
    M1 = L
    M2 = L[:]
    M1 is M2
    ```
    **What will this return?**
    
    > False
    

- **Consider the following code:**

    ```python
    import copy
    x = [1,[2]]
    y = copy.copy(x)
    z = copy.deepcopy(x)
    y is z
    ```
    **What will this return?**
    
    > False
    

- **Consider the following code:**

    ```python
    if False:
        print("False!")
    elif True:
        print("Now True!")
    else:
        print("Finally True!")
    ```
    **What does this print?**
    
    > “Now True!”
    

- **Consider the following code:**

    ```python
    if n%2 == 0:
        #blank#
    else:
        print("odd")
    ```
    **Assume that n is a previously defined integer. Can you replace the `#blank#` line so that the code prints `"even"` if `n` is even, and `"odd"` if `n` is odd?**
    
    > `print("even")`
    

- **Consider `bears = {"Grizzly":"angry", "Brown":"friendly", "Polar":"friendly"}`. Can you replace `#blank#` so the code will print a greeting only to friendly bears? Your code should work even if more bears are added to the dictionary.**

    ```python
    for bear in bears:
        if #blank#:
        print("Hello, "+bear+" bear!")
    else:
    print("odd")
    ```
    **Answer:**
    
    > `bears[bear] == "friendly”`
    

- **Consider the following code:**

    ```python
    is_prime = True
    for i in range(2,n):
        if n%i == 0:
            #blank#
    print(is_prime)
    ```
    **Can you fill in the `#blank#` line so the code will only print True if `n` is prime?**
    
    > `is_prime = False`
    

- **Consider the following code:**

    ```python
    n=100
    number_of_times = 0
    while n >= 1:
        n //= 2
        number_of_times += 1
    print(number_of_times)
    ```
    **What will this print?**
    
    > 7