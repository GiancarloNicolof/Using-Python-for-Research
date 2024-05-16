# Part 02: Sequence Objects

- **Consider the following tuple and index `(1,2,3)[-0]`. What will this return?**
    
    > 1
    
- **Consider the following tuple and index `(1,2,3)[-0:0]`. What will this return?**
    
    > ( )
    
- **Consider a list `x=[1,2,3]`. Which index corresponds to `2` in `x`?**
    
    > 1
    
- **Consider a list `x=[1,2,3]`. Enter the code below for how you would use the append method to add the number `4` to the end of list `x`.**
    
    > `x.append(4)`
    
- **What do list methods such as `reverse` and `sort` return?**
    
    > They return nothing because they are in-place methods, meaning they alter the content of the original list.
    
- **Consider the tuple `x=(1,2,3)`. How could you add the integer `4` to the end of the tuple?**
    
    > This is impossible. Tuples are immutable, so they can't be edited after they’ve been created.
    
- **Consider `x=(1,2,3)`. Use the `count` method to count the number of `3`s in `x`.**
    
    > `x.count(3)`
    
- **Consider again `x=(1,2,3)`. If you wanted the sum of the numbers in `x` using a single function, which command would you use?**
    
    > `sum(x)`
    
- **Which of the following prints type `tuple`?**
    
    > `type((2,))`
    
- **Why might you prefer to use a range over a list?**
    
    > Ranges take up less memory than lists because they do not hold all the numbers simultaneously.
    
- **Which of the following lines of code will fail to return the integers `0` through `9` in a single string?**
    
    > `str(range(10))`
    
- **Assume you have assigned `x` the string value of "125,000" (i.e., `x = "125,000"`). Can you find a string method that tests if `x` only contains digits?**
    
    > `x.isdigit()`
    
- **Let sets `x={1,2,3}` and `y={2,3,4}`. How could you get `{4}` from `x` and `y` using basic set operations?**
    
    > `y - (x & y)`
    
- **Consider again sets `x={1,2,3}` and `y={2,3,4}`. How could you get `{2, 3}` from `x` and `y` using basic set operations?**
    
    > `x & y`
    
- **Consider again sets `x={1,2,3}` and `y={2,3,4}`. How could you get `{1, 4}` from `x` and `y` using basic set operations?**
    
    > `(x | y) - (x & y)`
    
- **Consider again sets `x={1,2,3}` and `y={2,3,4}`. Which of the following lines of code will determine if all elements of `x` are in `y`?**
    
    > `x.issubset(y)`
    
- **Consider the dictionary: `age={'Tim':29, 'Jim':31, 'Pam':27, 'Sam':35}`. `age[0]` returns an error. Why?**
    
    > There is no key `0` in the dictionary.
    
- **Why may you not edit the key `"Tim"` to `"Tom"`?**
    
    > Dictionary keys are not mutable.
    
- **Which of the following data structures may be used as keys in a `dict?`**
    
    > Strings, Tuples