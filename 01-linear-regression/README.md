# Linear Regression

It's an analysis that is used to predict the value of a variable. The value that you'll be predicting is called the dependent variable. And the variables that you'll be using to predict the dependent variable are called independent variables.

Linear regression finds an equation line or surface that fits the given data so that it can predict dependent variable. It handles regression problems and provides continuous output.

## Linear Regression: The Syntax

Import the class containing the regression method from `sklearn.linear_model`

```python
from sklearn.linear_model import LinearRegression
```

Create an instance of the class

```python
LR = LinearRegression()
```

Fit the instance on the data and then predict the expected value

```python
LR = LR.fit(X_train , y_train)
y_ predict = LR.predict(X_test)
```