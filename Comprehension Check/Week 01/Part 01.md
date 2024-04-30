# Part 01: Objects and Methods

- **Python has two operating modes. Which are they?**
    
    > Both of the above.
    
- **Which version of Python will we focus on in this course?**
    
    > Python 3.
    
- **Which of the following statements is NOT correct?**
    
    > Python 2 code will always work with Python 3.
    
- **Python has immutable objects (e.g., strings and tuples) and mutable objects (e.g., dictionaries and lists). What does it mean for an object to be immutable?**
    
    > Its contents cannot be modified by the programmer after the object has been created.
    
- **Consider the following line of code:** `x = 4`. **In this assignment, what does the number `4` represent?**
    
    > The object value.
    
- **What is the difference between methods and data attributes of objects?**
    
    > Methods are functions associated with objects, whereas data attributes are data associated with objects.
    
- **Suppose that `math.sqrt` and `numpy.sqrt` had identical behavior. Are they the same function?**
    
    > No. Because they belong to different namespaces, Python treats them separately, regardless of their behavior.
    
- **After running `import numpy as np`, if you want to access the square root function (`sqrt()`) from the library `numpy`, which method would you use?**
    
    > `np.sqrt()`
    
- ***n factorial* is defined as the product of all integers 1,…,*n,* by definition 0! = 1. What is 4 factorial?**
    
    > 24
    
- **True or false: `random.choice` will not work on immutable types.**
    
    > False: `random.choice` only requires that the object has several values regardless of mutability.
    
- **Consider the expression `True and not False is True`. What will this return?**
    
    > `True`
    
- **What is the difference between `==` and `is`?**
    
    > `==` tests whether objects have the same value, whereas `is` tests whether objects have the same identity.