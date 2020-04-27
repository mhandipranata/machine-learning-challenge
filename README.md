# Predicting Exoplanet Exploration using Machine Learning Model

## Background
Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, we will create machine learning models capable of classifying candidate exoplanets from the raw dataset.

Steps:
1. Data cleaning
2. Train Test Split
3. Preprocess the raw data
4. Train and compare the models 


Libraries we are using: pandas, sklearn, joblib.



## 1. Data Cleaning 

By using Pandas, we read csv data (exoplanet_data.csv) and drop any 'N/A' in the data.  
   


## 2. Train Test Split

In this step, we select the columns to be included as X features, and select the categorical column as y. 

X = ['koi_disposition', 'koi_period', 'koi_time0bk', 'koi_impact', 'koi_duration',
    'koi_depth', 'koi_prad', 'koi_teq', 'koi_insol', 'koi_model_snr', 
    'koi_tce_plnt_num', 'koi_steff', 'koi_slogg', 'koi_srad', 'ra', 'dec',
    'koi_kepmag']
    
y = ['koi_disposition']

Depending on the models, we might need to encode the y categorical values to numbers (0 1 2) using LabelEncoder from sklearn library.

Using train_test_split from sklearn library, we will split the data randomly to X_train, X_test, y_train, y_test.



## 3. Preprocess the raw data

Depending on the models, we need to scale the features in X using MinMaxScaler from sklearn library.



## 4. Train and compare the models

  
**Model 1: K Nearest Neighbors Model**

Training Data Score: 0.6172038909021552
Testing Data Score: 0.5852402745995423

  
**Model 2: Logistic Regression Model**

Training Data Score: 0.6313179477398436
Testing Data Score: 0.6304347826086957

  
**Model 3: GridSearchCV Model**

Train Best score: 0.5872592027465192
Test Best score: 0.6018306636155606

  
**Model 4: Deep Learning Model**

Loss: 0.6803219386587427
Accuracy: 0.7110983729362488

  
**Model 5: Decision Trees and Random Forest Model**

Decision Trees Model Best Score: 0.6893592677345538
Random Forest Model Best Score: 0.7677345537757437


  
  
## Conclusion

Random Forest Model seems to have the best score compared with other models, and 0.7677 is quite a good number to predict.
If we have better information / domain knowledge regarding the data, we might be able to narrow down the features that affect the predictions.

