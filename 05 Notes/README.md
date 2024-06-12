
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