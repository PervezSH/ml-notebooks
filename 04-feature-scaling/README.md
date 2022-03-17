# Feature Scaling

Feature Scaling is a technique to standardize the independent features present in the data in a fixed range. It involves adjusting the variables scale. It is performed during the data pre-processing to handle highly varying magnitudes or values or units.
Distance-based algorithms like **KNN**, **K-means**, and **SVM** are most affected by the range of features. 

## Why do we need feature scaling?
Machine learning algorithm tends to weigh greater values, higher and considers smaller values as the lower values, regardless of the unit of the values. And feature scaling allows the comparison of variables with different scales.
Example: Comparing price 1 to 10 with number of shops 10,000 to 50000

## How to perform feature scaling?
There are many ways to perform feature scaling
- StandardScaler, also known as Standardization
- MinMaxScaler, also known as Normalization
- MaxAbsScaler
- Robust Scaler
- Quantile Transformer Scaler
- Power Transformer Scaler
- Unit Vector Scaler