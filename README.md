# Car Price Prediction

## Overview
This project focuses on predicting car prices using regression models. It involves evaluating various regression algorithms and identifying potential hyperparameters for tuning to improve model performance.

## Dependencies
The project relies on the following Python libraries:
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- xgboost
- statsmodels
- tabulate

You can install the dependencies using the following command:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost statsmodels tabulate


```python
import numpy as np  # Numerical computations
import pandas as pd  # Data manipulation
import missingno as mn  # Visualization of missing data patterns
from collections import Counter, OrderedDict  # Counting occurrences, ordered dictionaries

import matplotlib.pyplot as plt  # Basic plotting
import seaborn as sns  # Statistical data visualization

import statsmodels.api as sm  # Statistical models and tests
from scipy import stats  # Statistical functions

from sklearn.model_selection import train_test_split, GridSearchCV  # Data splitting, hyperparameter tuning
from sklearn.metrics import mean_squared_error, r2_score  # Evaluation metrics
from sklearn.linear_model import LinearRegression, Lasso, Ridge  # Regression models
from sklearn.svm import SVR  # Support Vector Regression
from sklearn.tree import DecisionTreeRegressor  # Decision tree modeling
from sklearn.ensemble import RandomForestRegressor, StackingRegressor  # Random forest, stacking models
import xgboost as xg  # Gradient boosting modeling

from tabulate import tabulate  # Tabulating results

import warnings  # Ignoring unnecessary warnings
warnings.filterwarnings('ignore')



Data Wrangling
numpy: For numerical computations
pandas: For data manipulation
missingno: For visualizing missing data patterns
collections.Counter: For counting occurrences
collections.OrderedDict: For ordered dictionaries
Data Visualization
matplotlib.pyplot: For basic plotting
seaborn: For statistical data visualization
Data Preprocessing
statsmodels.api: For statistical models and tests
scipy.stats: For statistical functions
Modelling
sklearn.model_selection.train_test_split: For splitting data
math.sqrt: For square root operation
sklearn.metrics.mean_squared_error, sklearn.metrics.r2_score: For evaluation metrics
sklearn.model_selection.GridSearchCV: For hyperparameter tuning
sklearn.linear_model.LinearRegression: For linear regression modeling
sklearn.linear_model.Lasso: For Lasso regression
sklearn.linear_model.Ridge: For Ridge regression
sklearn.svm.SVR: For Support Vector Regression
sklearn.tree.DecisionTreeRegressor: For decision tree modeling
sklearn.ensemble.RandomForestRegressor: For random forest modeling
sklearn.ensemble.StackingRegressor: For stacking models
xgboost: For gradient boosting modeling
Tabulating the Results
tabulate: For tabulating results
Remove Unnecessary Warnings
warnings: For ignoring warnings



# Regression Model Evaluation and Hyperparameter Tuning

## Overview
This project aims to evaluate various regression models and identify potential hyperparameters for tuning to improve model performance. The code utilizes popular regression algorithms such as Linear Regression, Lasso Regression, Ridge Regression, Support Vector Regression (SVR), Decision Tree Regression, Random Forest Regression, and XGBoost Regression.

## Dependencies
The following Python libraries are required to run the code:
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- xgboost
- statsmodels
- tabulate

You can install the dependencies using the following command:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost statsmodels tabulate


Based on the evaluation metrics, the performance of the regression models can be summarized as follows:

Multi Linear Regression:

Train RMSE: 3.956
Test RMSE: 3.815
Train R-squared: 0.930
Test R-squared: 0.858
Lasso Regression:

Train RMSE: 3.985
Test RMSE: 3.781
Train R-squared: 0.929
Test R-squared: 0.861
Ridge Regression:

Train RMSE: 3.956
Test RMSE: 3.815
Train R-squared: 0.930
Test R-squared: 0.858
Support Vector Regression (SVR):

Train RMSE: 11.282
Test RMSE: 6.921
Train R-squared: 0.428
Test R-squared: 0.533
Decision Tree Regression:

Train RMSE: 0.000
Test RMSE: 4.942
Train R-squared: 1.000
Test R-squared: 0.762
Random Forest Regression:

Train RMSE: 1.331
Test RMSE: 3.362
Train R-squared: 0.992
Test R-squared: 0.890
XGBoost Regression:

Train RMSE: 0.001
Test RMSE: 4.255
Train R-squared: 1.000
Test R-squared: 0.824
Conclusion:

Linear Regression-based models (Multi Linear, Lasso, and Ridge) show relatively similar performance with moderate RMSE and R-squared values.
Support Vector Regression (SVR) performs poorly compared to other models, with significantly higher RMSE and lower R-squared values.
Decision Tree Regression achieves perfect R-squared on the training data but performs poorly on the test data, indicating overfitting.
Random Forest Regression and XGBoost Regression outperform other models, showing lower RMSE and higher R-squared values on both train and test data.
Evaluation Metrics:

RMSE (Root Mean Squared Error): Measures the average deviation of predicted values from actual values. Lower RMSE indicates better model performance.
R-squared: Represents the proportion of variance in the dependent variable that is predictable from the independent variables. Higher R-squared values indicate better fit of the model to the data.



Conclusion


After evaluating several regression models for predicting car prices, we have observed varying performances across different algorithms. Linear regression-based models, including Multi Linear Regression, Lasso Regression, and Ridge Regression, showed moderate performance with relatively similar RMSE and R-squared values. Support Vector Regression (SVR) exhibited poorer performance compared to other models, indicating its limitations in capturing the underlying patterns in the data.

Decision Tree Regression demonstrated perfect R-squared on the training data but performed poorly on the test data, suggesting overfitting. In contrast, Random Forest Regression and XGBoost Regression outperformed other models, achieving lower RMSE and higher R-squared values on both the train and test datasets.

In conclusion, Random Forest Regression and XGBoost Regression appear to be promising models for predicting car prices, offering better accuracy and generalization compared to other algorithms. Further fine-tuning of hyperparameters and regularization techniques could potentially enhance the performance of these models even further.