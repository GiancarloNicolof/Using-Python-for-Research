
# Using Python for Research
---

## Normal Distribution

A continuous probability distribution (means that can take any value within a specific range) that is symmetrical and bell-shaped. Characterized by two parameters:
- $\mu$ (mean): central value of an array of data after it has been sorted.
- $\sigma$ (standard deviation): how spread out the numbers in a data set are around the mean of the set.
### Standard Deviation

When we have the data for the entire group we’re interested in:  

$$
\sigma = \sqrt{\frac{\sum(x_{1}-\mu)^2}{N}}
$$
  
- $x_i$ → each data point
- $\mu$ → data points mean
- $N$ → number of data points

Small standard deviation → data points close to the mean
Large standard deviation → data points are spread out

### Probability Density Function (PDF)

Describes the probability of a random variable of taking a particular value or falling within a specific range of values in a continuous probability distribution.

$$
f(x) = \frac{1}{\sqrt{2\pi\sigma^2}}e^-{\frac{(x-\mu)^2}{2\sigma^2}}
$$

- $\mu$ → mean of the distribution
- $\sigma$ → standard deviation
- $e$ → base of the natural logarithm

---
## Standard Normal Distribution

<img src="Images/normal_curve.png" width="300">

Normal distribution with 
- $\mu = 0$
- $\sigma = 1$

Characteristics:
- Bell-shaped curve
- Symmetric around the mean
- 95% of data falls within two standard deviations

### Z-Score

Represents how many standard deviations an element is from the mean.

$$
z = \frac{X-\mu}{\sigma}
$$

- $X$ → value from the data set

---

## **k-Nearest Neighbors (kNN)**

1. **Points have coordinates and label or numerical value.**
2. **The number `k` represents how many neighbors you will look at when making the prediction.**
3. **Measure the distance between the new point and the rest points in the dataset.**
4. **Sort the distances and pick the `k` closest points.**
5. **Calculate the average of the values of these `k` nearest neighbors and use this average as the prediction for the new point.**

---

## Supervised Learning 

- Input data is paired with the corresponding output data.
- Output data provided by supervisor (human or another algorithm).
- Objective is to learn to associate the input with the output.

Divided into 2 groups based on their output:
1. Quantitative output → **Regression Problem**
2. Qualitative output → **Classification Problem**

The input can be a mix of quantitative and qualitative data for both groups.

### Regression Setting

<img src="Images/regression_setting.jpg" width="300">

The goal is to predict the value of $y$ given an $x$.
1. If there are points corresponding to that $x$, we return the mean of those values.
2. If there are no corresponding values, we look at the observations close to that $x$.
3. We return the average of those values.

$$
E(Y|\ \underline{\overline{x}} = x)
$$

A conditional average taking over all points that share at the value of x.

### Classification Setting

<img src="Images/classification_setting.jpg" width="300">

Values are either 1 or 0. We estimate the probability of $y$ belonging to either 1 or 0.

$$
P(Y = 0 | X = x)
$$

$$
P(Y=1 | X = x)
$$

The largest probability is going to be the prediction for $x$. 

---

## Unsupervised Learning

- Only input are provided.
- Objective is to learn relationships and structure from the input.

---

Variables are usually of 2 types:
1. **Quantitative**: numerical values. Their range depends on the units used.
2. **Qualitative**: categorical values. There can be any number of categories.
Numerical values can be turned into categorical values by introducing ranges (e.g. <$30.000 → low income).

The objective of both Regression and Classification problems is to find a function $f$ that, given an input $x$, it finds the output $y$.

$$
y = f(x)
$$

**Loss function** → measures for far the prediction of $y$ for a given $x$ is from the true observed value of $y$.

**Square Error Loss (MSE)** → The most common loss function for Regression problems. It measures the average squared difference between the actual (true) values and the predicted values by a model.

**0-1 Loss function** → The most common loss function for Classification problems. For a given $x$, we calculate the probability of each class and we then assign the observation to the class with the highest probability.

---
## Simple Linear Regression

Statistical technique used to understand the relationship between two continuous variables. It models the relationship between a dependent variable (response variable) and an independent variable (predictor variable) by fitting a linear equation to the observed data.

$$
Y = \beta_{0} + \beta_{1}X + \varepsilon
$$

- $Y$ and $X$ are random variables
- $\beta_0$ → intercept (value of $Y$ when $X = 0$)
- $\beta_1$ → slope (the change in $Y$ for a one-unit change in $X$)
- $\epsilon$ → error term (difference between observed and predicted values of $Y$)

Using training data, we can produce estimates $\hat{\beta_0}$ and $\hat{\beta_1}$ and predict future values of $y$.

$$
\hat{y} = \hat{\beta_{0}} + \hat{\beta_{1}}x + \varepsilon 
$$

The hats indicate they are estimated parameters (estimated using data).

### Least Squared Criterion

Used to find the best straight line that fits a set of data point in a graph.
1. Looks at how far from the line each data point is.
2. Squared the distances (to make them all positive) the sums them up.
3. The best line is the one that makes the total (RSS) as small as possible.

**Residual** → difference between the observed value ($y_i$) and predicted value ($\hat{y_i}$).

$$
e_{i}= y_{i} - \hat{y_{i}}
$$

---
## Sampling distribution of the parameter estimates

Represents the variability we would expect in the parameter estimates if we repeat the same sampling process multiple times on the same population.
1. If we take a sample from a population and calculate an estimate of a parameter, that estimate is rarely exactly equal to the true parameter value due to sample-to-sample variability.
2. Calculating the parameter estimate each time from many random samples of the same size from the population, we obtain a distribution of calculated values.
3. The sampling distribution describes how those sample estimates are distributed around the true parameter value in the population.

**Standard Error (SE)** → It measures the dispersion of the sample statistic from the true parameter value in the population. It provides information about the precision of the estimate.

$$
\hat{\beta_{1}} \pm 1.96 \times SE
$$

This gives the “95% confidence interval”, meaning 95% of the data in contained in this range.

### Total Sum of Squares (TSS)

It quantifies the overall deviation of the observed values from their mean.

$$
TSS = \sum_{i=1}^n (y_{i} - \overline{y})^2
$$

- $y_i$ → observed value for the $i$-th observation.
- $\overline{y}$ → mean of the observed values  
  
Represents the total variation in the dependent variable that needs to be explained by the model.

### Residual Sum of Squares (RSS)

It quantifies the deviation of the observed values from the predicted values.

$$
RSS = \sum_{i=1}^n (y_{i} - \hat{y_{i}})^2
$$

- $y_i$ → observed value for the $i$-th observation.
- $\hat{y_{i}}$ → predicted value for the $i$-th observation.

Represents the portion of the total variability that the model fails to explain.

### Variance Explained (R-squared)

Represents the proportion of the total variability that is explained by the model. It ranges from 0 to 1.

$$
R^2 = 1 - \frac{RSS}{TSS}
$$

If the model if useful, the RSS should be smaller than the TSS.

---
## Multiple Linear Regression

Models the relationship between a single dependent variable and two or more independent variables.

$$
Y = \beta_{0} + \beta_{1} X_{1} + \dots + \beta_{p}X_{p} + \varepsilon
$$

- $Y$ → dependent variable
- $X_1, \dots, X_p$ → independent variables
- $\beta_o$ → intercept
- $\beta_1, \dots, \beta_p$ → coefficients for each independent variable
- $\varepsilon$ → error term

A unit change the value of $X_{k}$ is associated with a change $\hat{\beta_k}$ in the value of the outcome $y$, while keeping all other predictors fixed.

---
## Mean Squared Error

Common measure used to evaluate the accuracy of a predictive model.

$$
MSE = \frac{1}{n} \sum_{i=1}^n (y_{i} - \hat{y_{i}})^2
$$

A smaller MSE indicates a better fit of the model to the data. If we use the test dataset to make the measurements, we get the Test MSE.

### Training Error Rate

Proportion of errors the model makes on the training dataset.

$$
\text{Training Error Rate} = \frac{\text{Number of Incorrect Predictions on Training Data}}{\text{Total Number of Training Examples}}
$$

High training error rate indicates that the model has not learned the training data well. A very low training error rate could indicate overfitting, where the model performs well on training data but may not generalize well to new data.

### Test Error Rate

Proportion of errors the model makes on the test dataset, which consists of new, unseen data.

$$
\text{Test Error Rate} = \frac{\text{Number of Incorrect Predictions on Test Data}}{\text{Total Number of Test Examples}}
$$

A lower test error rate indicates better generalization performance.

---
## Logistic Regression

Statistical method used for binary classification problems, where the goal is to predict one of two possible outcomes.

**Conditional class probabilities** → represent the probabilities of each class given the input features.

If there are only two classes, usually we use `0` and `1` as labels, so the output $y$ is always either `0` or `1`.

$$
P(x) = P(y=1|x)
$$

The probability that $Y$ is equal to 1 given the value of $X$.
If $Y$ is not equal to 1, it must be 0.

$$
P(y=0|x) = 1 - P(x)
$$

Using Linear Regression would give us probabilities that could be greater than 1 or less that 0, while with Logistic Regression the probability is constrained between 0 and 1. We can modify Linear Regression to make it work.

$$
\log \frac{P(x)}{1-P(x)} = \beta_{0} + \beta_{1} x_{1}
$$

Logistic Regression is a linear model that models probabilities on a non-linear scale.
- $\frac{P(x)}{1-P(x)}$ → odds of that event. 

Odds can go from 0 to $\infty$ (ratios of two never negative probabilities). $\log$ odds can vary from $-\infty$ to $+\infty$, so we can now use a linear model to model the left hand-side expression.

If we add multiple predictors to the right hand-side of the expression, we get the **multiple logistic regression**. The coefficients in this case must be estimated from data, usually done using the method of maximum likelihood that finds parameter estimates that make the observed data maximally likely.