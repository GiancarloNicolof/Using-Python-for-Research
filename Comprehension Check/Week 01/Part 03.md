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

- **Consider the following code:**
    ```python
    sum([i**2 for i in range(3)])
    ``` 
    **What will this output?**
    > 5

- **How can you use a list comprehension, including `if` and `for`, to sum the odd numbers from `0` through `9`?**
    > `sum([i for i in range(10) if i % 2 == 1])`

- **Consider the following code:**
    ```python
    F = open("input.txt", "w")
    F.write("Hello\nWorld")
    F.close()
    lines = []
    for line in open("input.txt"):
        lines.append(line.strip())
    print(lines)
    ``` 
    **What does this print?**
    > `['Hello', 'World']`

- **Consider the following function:**
    ```python
    def modify(mylist):
        mylist[0] *= 10
        return(mylist)
    L = [1, 3, 5, 7, 9]
    M = modify(L)
    M is L
    ``` 
    **What is the value of the final line?**
    > `True`

- **Consider the function `intersect()` defined in the previous video, 1.3.8: Writing Simple Functions. What will `intersect([1,2,3], [3,4,5,6,7])` return?**
    > `[3]`

- **Consider the following code:**
    ```python
    def is_vowel(letter):
        if #blank#:
            return(True)
        else:
            return(False)
    ``` 
    **Can you replace `#blank#` in the second line so `is_vowel` becomes a function that takes a letter as input and prints whether a letter is a vowel (in `"aeiouy"`)?**
    > `letter in "aeiouy"`  

- **Consider the function call `is_vowel(4)`. Why would this not work?**
    > `4` is not a `string`, and Python cannot test if an `int` is in a `string`.

- **Consider the following following proposed emendation of `is_vowel`:**
    ```python
    def is_vowel(letter):
        if type(letter) == int:
            letter = str(letter)
        if letter in "aeiouy":
            return(True)
        else:
            return(False)
    ``` 
    **Does this properly accommodate objects of type `int` for use with `is_vowel`? For example, will `is_vowel(4)` produce a correct answer?**
    > Yes

- **Recall that *n*! ("*n* factorial") is defined as the product of all integers 1,...,*n*. Additionally, by definition, 0! = 1.**
    **Let's create a factorial function. Consider the following code:**
    ```python
    def factorial(n):
        if n == 0:
            return 1
        else:
    	    N = 1
            for i in range(1, n+1):
                #blank#
        return(N)
    ``` 
    **Can you fill in the `#blank#` to complete the function as described above?**
    > `N *= i`

- **When you encounter an error in Python, what should you do?**
    > All of the above.