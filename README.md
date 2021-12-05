# DA-Project

## Abstract
The main objective of this project is to aid in understanding the impact of various medical statistics and environmental conditions on the Life Expectancy of the citizens across a multitude of countries. The primary aim of the project is to use regression analysis to help in the prediction of Life Expectancy based on a few key features obtained via Exploratory Data Analysis and Feature Selection. The data used in this project has been collected from the World Health Organisation and includes various attributes such as Health Expenditure, Air Pollution, Unsafe Sanitation, GDP and so on. The project additionally aims to explore life expectancy as a function of time. We aim to develop a clustering strategy that breaks away from this binary classification. We benchmark these models against a gradient boosting model and its metrics

As a part of this project the following models were built to analyse and predict Life expectancy: 
1. Multiple Linear Regression
2. Decision Tree Regression
3. Random Forest Regression
4. Extreme Gradient Boosting Regression 
5. Holt Exponential Smoothing 
6. K-Means Clustering 

## Preprocessing 
As a part of preprocessing two datasets had to be integrated to create the dataset for this model. This was followed by data cleaning which involved handling null and duplicate values. The data was sanitised to ensure proper formatting. The data was winsorised to handle outliers. Since the dataset covers a wide variety of countries, there was bound to be a large range of values for the numerous columns. The data were standardised using the standard scaler to ensure that the mean is 0 and the standard deviation is 1. Finally, Principal component analysis was done to reduce the dataset from 48+ features to 26 features that are useful for modelling. 

## Modelling 
The regression models were built with the agenda of predicting the life expectancy based on the various health, socio-economic and environmental features present in the dataset. The time series model was built to model the data to time. Finally, the clustering model was built to help understand if one could break away from the binary classification of countries into developed and developing. 

### Each model is segregated into its folder under the models' folder. The models are developed in notebooks and the data will have to be manually loaded for the same during the execution 

### Regression models 
The linear regression and decision tree regression model were built first. However, they weren't successful in predicting the values of Life Expectancy due to the overfitting of data. Post this, the random forest model was built which was able to model the data with a decent r2 and rmse value. Finally, we built the gradient boosting model to help tackle the non-linear nature of data. The metric used for comparing these models is as mentioned in the below table. 

 |Model | R2 score     | RMSE
 |Linear Regression    | 0.88   | 3.40
 | Decision Tree Regression| 0.85 | 3.69
 | Random Forest Regression | 0.93 | 2.65
 | Extreme Gradient Boosting | 0.92  | 2.44
 
### Time Series Forecasting
The preprocessing for time series forecasting involved using decomposition graphs to identify the four components and using the augmented dickey fuller test to check for stationarity. We notice that the model has an evident trend line but lacks seasonality and cyclic component. So we use Holt's Exponential Smoothing to model the data. The values obtained are mentioned below. 

 |Level Coefficient | Trend Coefficient     | RMSE
 |0.8   | 0.2  | 0.205
 
### Clustering 
We use K-Means clustering to cluster the data into clusters based on the elbow method. We also use the silhouette score to determine the accurate number of clusters. We see that these metrics dictate that the model can be grouped into 8 clusters over the binary classification. 

## Conclusion 
In conclusion, we see that data could be modelled and predicted with only socio-economic, health and environmental conditions using regression and doesn't depend on the binary classification of the state. We also see that the data can be effectively modelled as a time series model using Holt's exponential smoothing method. We also provide proof for the fact that one could easily break away from the binary classification of countries. 
