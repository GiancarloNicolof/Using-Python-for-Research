# Part 01: Linear Regression

- **What is the difference between supervised and unsupervised learning?**
	> Supervised learning matches inputs and outputs, whereas unsupervised learning discovers structure for inputs only.

- **What is the difference between regression and classification?**
	> Regression results in continuous outputs, whereas classification results in categorical outputs.

- **What is the difference between least squares loss and `0-1` loss?**
	> Least squares loss is used to estimate the expected value of outputs, whereas `0-1` loss is used to estimate the probability of outputs.

- **The code from the previous video is as follows:**
	```python
	import numpy as np
	import scipy.stats as ss
	import matplotlib.pyplot as plt
	
	n = 100
	beta_0 = 5
	beta_1 = 2
	np.random.seed(1)
	x = 10 * ss.uniform.rvs(size=n)
	y = beta_0 + beta_1 * x + ss.norm.rvs(loc=0, scale=1, size=n)
	```
	Run this code on your computer.
	What is the approximate mean of `x` and `y`, respectively?
	> Mean `x` = 4.9, mean `y` = 14.8

- **What is the difference between $Y$ (capital letter) and $y$ (lowercase letter)?**
	> $Y$ is a random variable, whereas $y$ is a particular value.

- **The following code implements the residual sum of squares for this regression problem:**
	```python
	def compute_rss(y_estimate, y):
		return sum(np.power(y-y_estimate, 2))
	
	def estimate_y(x, b_0, b_1):
		return b_0 + b_1 * x
	
	rss = compute_rss(estimate_y(x, beta_0, beta_1), y)
	```
	Using the data from CC 5.1.2, run the code above. What is the approximate value of $rss$?
	> 82

- **Is the best estimate for the slope *exactly* the same as the true value 2 (when rounded to two decimal places)? Rerun the code in the video, but use a finer grid for the search by specifying**
	`slope = np.arange(-10, 15, 0.001)`
	Which of the following characterizes the new estimate for the slope?
	> Still exactly 2

- **If the true intercept were negative but the regression model did not include an intercept term, what would that imply for the estimated slope?**
	> The estimated slope would be likely be lower that the true slope.

- **What does an estimated intercept term correspond to?**
	> The estimated outcome when the input is set to zero.

- **What does an estimated slope term correspond to?**
	> The change in the estimated output when the input changes by one unit.

- **You could create several datasets using different seed values and estimate the slope from each. These parameters will follow some distribution.**
	What is the name used for this distribution?
	> The sampling distribution of the parameter estimates.

- **If the $R^2$ value is high, this indicates:**
	>   a good fit: the residual sum of squares is low compared to the total sum of squares.

- **Consider a multiple regression model with two inputs. The model predictions for the output $y$ are given by**
	$\hat{y} = \hat{\beta}_{0} + x_{1} \hat{\beta}_{1} + x_{2} \hat{\beta}_{2}$
	$\beta_1$ and $\beta_2$ have been estimated from data. If we assume $\hat{\beta}_1 = 1$ and $\hat{\beta}_2 = 3$. 
	What is the interpretation of $\hat{\beta}_1 = 1$?
	> The change in the predicted outcome if $x_1$ is increased by 1, holding $x_2$ constant.

- **Consider the model and parameters in Question 1. For a given expected output prediction $\hat{y}$, what would be the expected change in the prediction value if you increased $x_1$  by 1, and decreased $x_2$ by 3?**
	> -8

- **In the video, we estimated the values of three parameters. Which of these estimates is the closest to its true value?**
	> The estimated first slope, $\beta_1$.

+ **When evaluating the performance of a model in a regression setting on test data, which measure is most appropriate?**
	> Test MSE

- **When evaluating the performance of a model in a classification setting on test data, which measure is most appropriate?**
	> Test error rate

- **How do we expect an model that was overfit on the training data to perform on testing data?**
	> It will likely perform worse on the testing data.

- **What is the primary motivation for splitting our model into training and testing data?**
	> By evaluating how our model fits on unseen data, we can see how generalizable it is.