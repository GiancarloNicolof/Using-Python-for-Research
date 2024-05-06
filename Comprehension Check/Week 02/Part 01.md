# Part 01: Scope Rules and Classes

- **Consider the following code:**
    ```python
    def increment(n):
        n += 1
        print(n)

    n = 1
    increment(n)
    print(n)
    ```
    **What will this print? Note that here, we separate lines of output with `;`.**
    > 2; 1

- **Consider the following code:**
    ```python
    def increment(n):
        n += 1
       #blank#

    n = 1
    while n < 10:
        n = increment(n)
    print(n)
    ```
    **Fill the `#blank#` to ensure this print `10`.**
    > `return n`