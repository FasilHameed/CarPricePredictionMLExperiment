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



Conclusion
Among the evaluated models, Support Vector Regression (SVR) showed the best overall performance on the test dataset. However, all models except Decision Tree and XGBoost regressions exhibited signs of overfitting and may benefit from further tuning or regularization.

Hyperparameter Tuning Scope
Lasso Regression and Ridge Regression: Fine-tune the alpha hyperparameter to optimize regularization strength.
Support Vector Regression: Tune hyperparameters such as C and gamma through grid search or random search.
Random Forest Regression: Optimize n_estimators and max_depth to improve performance and mitigate overfitting.
XGBoost Regression: Fine-tune hyperparameters like n_estimators, max_depth, and learning_rate to enhance model performance and prevent overfitting.