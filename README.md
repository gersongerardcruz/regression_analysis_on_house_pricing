# Regression Analysis on House Pricing
This repository contains a jupyter notebook focusing on Kaggle's House Pricing Dataset. Exploratory Data Analysis, Data Preprocessing, and Modelling was performed using Pandas, Numpy, Seaborn, and Scikit-learn.

## Dataset
The dataset consists of a train and test set gotten from Kaggle's Datasets at this link: https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data

For more information about the datasets, check out the data_description.txt file!

## Project Features

### Exploratory Data Analysis
* Pandas functions were used to gather information about the statistical summary of the dataset, missing data points, and quantitative and qualitative features
* Seaborn and Matplotlib functions were used to visualize the relationship between the target variable **Sale Price** to other quantitative features.

### Data Cleaning and Preprocessing
* Imputers were utilized to replaced certain features with simple mean, median, and mode
* Lambda functions were used to replaced multiple NaN rows with the appropriate **None** or **NA** categorical data
* Category encoders were used to replace categorical features. Binary and Pandas' Get_Dummies were the main encoders dependent on the number of unique values per column.

### Data Modelling
* Scikit-learn's StandardScaler was used to scale the data to avoid outliers affecting the quality of the model.
* Numpy's logarithmic transformation was used to make the target data follow a normal distribution, as required in any regression analysis
* Skikit-learn's LinearRegression, GradientBoostingRegressor, and HistGradientBoostingRegressor the main models in this notebook.
* Hyperparameter tuning was performed via the selection of the best learning rate for the GradientBoosting Regressors. 
* The main metric in this notebook was the Root Mean Squared Error (RMSE), which after logarithmic transformation, decreased from an average of 30000 to 0.11

### Recommendations
For future iterations of this project, the following improvements can be done:

* More use of hyperparameter tuning to select best features for the models and the use of more models in doing the training and validation
* For Data Cleaning and Preprocessing, the results of directly removing uncorrelated variables can be explored
* The use of model ensembling to further decrease the root mean squared error
