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

- **Consider the following code:**
    ```python
    class NewList(list):
        def remove_max(self):
            self.remove(max(self))
        def append_sum(self):
            self.append(sum(self))

    x = NewList([1,2,3])
    while max(x) < 10:
        x.remove_max()
        x.append_sum()

    print(x)
    ```
    **What will this print?**
    > Nothing: this program will never halt.