# Polynomial Regression

Polynomial Regression is another pre-processing trick besides the standard scalar or any of the other pre-processing that we've done is to create new features out of the ones that we already have.

## Polynomial Features: The Syntax

Importing the class containing the transformation method.

```python
from sklearn.preprocessing import PolynomialFeatures
```

We create an instance of our class.

```python
polyFeat = PolynomialFeatures(degree=2)
```

Create the polynomial features and then transform the data.

```python
polyFeat = polyFeat.fit(X_data)
X_poly = polyFeat.transform(X_data)
```
## Why Polynomial Regression?

Linear regression only identifies a linear relationship between independent and dependent variables. So, if we have non-linear data then linear regression won't be able to draw a best-fit line. Hence, we use polynomial regression to overcome this problem, which helps determine the curvilinear relationship between independent and dependent variables.

## Choosing the Level of Complexity

![level-of-complexity.jpg](/05-polynomial-features-and-regularizations/images/level-of-complexity.jpg)

Our goal here is to fit a polynomial model to each one of our sample points. This problem can be framed as a choice between different model complexity.

The above model involves polynomials of different degrees, `1st` order, `4th` order, and `15th` order.

The error function continuously decreases as we increase the polynomial degree. Even though this is actually deviating from the actual underlying function.

# Regularization

The power of regularization will ultimately be one of the major keys to ensuring that we choose a model that will give us the balance between bias and variance within our models.

### High Bias

The tendency for a model to miss the true values when trying to predict.

This happens due to either missing information or overly simplistic models. We can associate high bias with the concept of underfitting or there not being enough complexity in our model.

### High Variance

The tendency for our predictions to fluctuate dramatically.

This happens when we make our model way too complex by adding more and more features. We can associate high variance with the concept of the overfitting model.

### The trade-off between Bias and Variance

The idea is that model adjustment that decreases bias will often increase variance, and vice versa. We can assume a high bias is going to lead to too simple of a model. And high variance is going to lead to too complex of a model. Finding the best model means choosing the right level of complexity.

## Regularization Techniques
> 💡Ridge and Lasso's regression are some of the simple techniques to reduce model complexity and prevent over-fitting which may result from simple linear regression.

**Lasso regression** is a regularization technique. It is used over regression methods for a more accurate prediction. This model uses shrinkage. Shrinkage is where data values are shrunk towards a central point as the mean.

**Ridge regression** is a model tuning method that is used to analyze any data that suffers from multicollinearity. This method performs L2 regularization. When the issue of multicollinearity occurs, least-squares are unbiased, and variances are large, this results in predicted values being far away from the actual values.