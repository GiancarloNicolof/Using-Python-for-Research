# Part 03: Random Forest

- **The goal of a tree-based method is typically to split up the predictor or feature space such that:**
	> data within each region are as similar as possible

- **Part 1.** For classification, how does a decision tree make a prediction for a new data point?
	> It returns the mode of the outcomes of the training data points in the predictor space where the new data point falls.

	**Part 2.** For regression, how does a decision tree make a prediction for a new data point?
	> It returns the mean of the outcomes of the training data points in the predictor space where the new data point falls.

- **Random forests get their name by introducing randomness to decision trees in two ways, once at the data level and once at the predictor level.**
	**Part 1.** How is randomness at the data level introduced?
	> Each tree gets a bootstrapped random sample of training data.
	
	**Part 2.** How is randomness at the predictor level introduced?
	> Each split only uses a subset of predictors.

- **Part 1.** In a classification setting, how does a random forest make predictions?
	> Each tree makes a prediction and the mode of these predictions is the prediction of the forest.

	**Part 2.** In a regression setting, how does a random forest make predictions?
	> Each tree makes a prediction and the mean of these predictions is the prediction of the forest.