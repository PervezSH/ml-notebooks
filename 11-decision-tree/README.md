# Decision Tree 🎄

Decision tree splits the dataset into two datasets at every set, for which the decision is going to be easier, and then continue to iterate. It splits data using impurity measures. They are greedy algorithms and are not based on statistical assumptions.

The most common splitting impurity measures are **Entropy** and **Gini index**.

The great advantages of decision trees are that they are really easy to interpret and require no data preprocessing.

This idea can be used in predicting quantities instead of classes as well. And rather than decision trees, they will be called **regression trees**.

## The Approach 🌪️
What the decision tree does is select a feature and ask a question with a true, or false answer. Given whether, or not, we answer true, or false to a given question split data into those two subsets. And continues to do so until leaf nodes are pure i.e., only one class remains. However, this idea will often overfit.

Another idea is we can enter a max depth and then stop or prune our tree at that depth. And at that depth, we don't allow it to grow any further.

The third idea is we can keep going until a predefined performance metric is achieved. For example, if the classification has a certain accuracy, then we would stop.

Decision tree uses greedy search to find the best split. At every step, it finds the split that induces the biggest information gain.

## Decision Tree Classifier: The Syntax

```python
# import the class containing the classification method
from sklearn.tree import DecisionTreeClassifier

# create an instance of the class
DTC = DecisionTreeClassifier(criterion='Gini', max_features=10, max_depth=5)

# fit the instance on the data and then predict the expected value
DTC = DTC.fit(X_train, y_train)
y_predict = DTC.predict(X_test)
```
We have here some hyperparameters to help regularize this equation. You can look at the [documentation](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html) to know more about them.

> 💡 In order to perform regression, we can import `DecisionTreeRegression`.