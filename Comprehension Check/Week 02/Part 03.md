# Part 03: Matplotlib and Pyplot

- **What does `plt.show()` do?**
    > Show a plot that is already created.

- **What does `plt.plot([0,1,2], [0,1,4], "rd-")` do?**
    > A plot of two connected lines, with red diamonds at the junctures.

- **Consider the following code:**
    ```python
    x.logspace(0, 1, 10)
    y = x**2
    plt.loglog(x, y, "bo-")
    ```
    What does this return?
    > A logarithmic plot that looks like a straight line with equal spacing. 

- **Whis will have wider bins, `np.linspace(-5, 5, 21)` or `np.linspace(-5, 5, 201)`?**
    > `np.linspace(-5, 5, 21)`

- **What will `plt.subplot(333)` do?**
    > Create a smaller subplot in the top right of the figure.

- **Will `plt.subplot(3, 3, 3)` create a different plot from `plt.subplot(333)`?**
    > No