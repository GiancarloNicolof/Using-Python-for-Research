# Part 04: Randomness and Time

- **Use `random.choice` and `range` to generate a random integer from 0-9.**
    > `random.choice(range(0,10))`

- **What will `random.choice(list([1, 2, 3, 4]))` produce?**
    > A value from 1 to 4, selected at random.

- **Which of the following lines of code takes the sum of 10 random integers between 0 and 9?**
    > `sum(random.choice(range(10)) for i in range(10))`