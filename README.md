# Prediction-of-House-Prices-in-Iowa
Using predictive modelling to predict house prices in Iowa
This project is based on the Kaggle competition, House Prices: Advanced Regression Techniques (https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
The aim of this project is prediction of house prices by using data with 79 explanatory variables describing almost every aspect of residential homes in Ames, Iowa.

House Prices (Python) Script:
I tried out various machine learning algorithms like XgBoost, Random Forest, Logistic Regression etc. to find out which model is best suited for this dataset. The XgBoost model performed the best, and its predictions yielded a score of 0.12432 on the Public Leaderboard on Kaggle.
(Side Note: Yes, we can use Logistic Regression for regression problems. Logistic Regression isn't a classification algorithm unless coupled with a classification rule. It's the classification rule which makes it dichotomous.)

House Prices (R) Script:
I have done some comprehensive exploratory data analysis (EDA), and tried to understand the nuances of the data by doing univariate and multivariate analysis of variables. Next, I tried to clean the data by imputing missing values, removing outliers, binning some variables, label encoding categorical variables wherever possible, and creating dummy variables. I have also done feature engineering, where I introduced new variables using already present variables which I felt would contribute to the model.
My goal was to transform all of the data into numeric, while preserving as much information from the categoric variables as I used a gradient boosting method (XgBoost). As XgBoost has trouble with extrapolation I used ridge, lasso and elastic-net regularization, which also accounts for a lot of the multicollinearity in the data. Then I built an ensemble model by taking a weighted average of the outcome of the 4 models.

I validated the models on in-sample data, with RMSE as metric. The XgBoost model gave a score of 7472.43, while the ridge, lasso and elastic-net regularization models gave a score of 17289.25, 18192.0042 and 17321.09 respectively. I used a weight ratio of 3:1:1:1 for the ensemble model.

I managed to get a score of 0.12142 on the Kaggle competition after submitting the predictions of my ensemble model.
