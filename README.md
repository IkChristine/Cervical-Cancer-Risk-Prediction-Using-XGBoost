# Cervical-Cancer-Risk-Prediction-Using-XGBoost
Extreme gradient boosting algorithm (Xgboost) 
<div class="alert alert-block alert-info" style="margin-top: 20px">

## Introduction

- Cervical cancer kills about 4,000 women in the U.S. and about 300,000 women worldwide. Due to increased medical screening, cervical cancer death rate has been reduced by 74% between 1955 to 1992. 
Studies have shown that high sexual activity Human Papillloma Virus (HPV) is one of the key factors that increases the risk of having cervical cancer. 

- The presence of hormones in oral contraceptives, having many children, and smoking increases the risk of developing cervical cancer, particularly in women infected with HPV. Also, individuals with weak immune systems eg. HIV/AIDS, have a high risk of HPV.

- By leveraging maching learning and AI, cervical cancer death rate can be reduced with early detection and diagnosis.
- <p>&nbsp;</p>

### XGBoost Algorithm
Extreme gradient boosting algorithm (Xgboost) offers solid robustness and computational efficiency.
XGBoost is a supervised learning algorithm that implements the gradient boosted trees alogorithm. Boosting works by building a model from the training data, then the second model is built based on the mistakes (residuals) of the first model. The algorithm repeats until the maximum number of models have been created to provide better predictions. 
<p>&nbsp;</p>


## Project Goals
- This project aims to build and train an XGBoost model to predict cervical cancer in 859 patients.
- <p>&nbsp;</p>

# Dataset
- The dataset was obtained from Hospital Universitario de Caracas in Caracas, Venezuele and it contains demographic information, habits, and historical medical records of 858 patients.

Input features will be passed to into the XGBoost model to predict the biospsy outcome. 

- Input Features
1. Age
2. Number of pregnancies
3. Smoker status
4. IUDs
5. STD status


- Target variable
1. Biospy Status (Y/N)
<p>&nbsp;</p>

# #


Data Sources
- https://www.kaggle.com/loveall/cervical-cancer-risk-classification
- https://archive.ics.uci.edu/ml/datasets/Cervical+cancer+%28Risk+Factors%29

## Analysis Highlights

![image](https://github.com/IkChristine/Cervical-Cancer-Risk-Prediction-Using-XGBoost/assets/104997783/6457f38d-d6c4-4bfd-94f0-77b4e26159a4)

<p>&nbsp;</p>

## Conclusion
model = xgb.XGBClassifier(learning_rate = 0.1, max_depth = 5, n_estimators = 10)
* The XGBoost model achieved a 98% accuracy on the training data
* 93.02% accuracy score on testing data
* 96% on precision and recall for class zero (0), which is great but 50%
precision and recall for class 1 which is not good, and therefore can be improved.
* The XGBoost model achieved an overall 93% accuracy score
* The model correctly classified 77 samples (True Negative) and 3 samples (True Positive), however it 
misclassified 3 samples (False Positive) and 3 samples (False Negative).

![image](https://github.com/IkChristine/Cervical-Cancer-Risk-Prediction-Using-XGBoost/assets/104997783/629317f6-4b78-4e6a-8e2e-1ae2bb9eda37)


After the model was retrainied with 10X the number of estimators and tree depth
model = xgb.XGBClassifier(learning_rate = 0.1, max_depth = 50, n_estimators = 100)

* The retrained model achieved a 98.8% accuracy on the training data
* a 94% accuracy score on testing data
* it remained at 96% predicton score for class 0, but increased to a 57% precision score for class 1
* It increased to 98% recall score for class 0 and decreased to a 36% recall score for class 1
* achieved a slightly higher accuracy score of 94%
* The model correctly classified 160 samples (True Negative) and 4 samples (True Positive), however it 
misclassified 7 samples (False Positive) and 4 samples (False Negative).

![image](https://github.com/IkChristine/Cervical-Cancer-Risk-Prediction-Using-XGBoost/assets/104997783/2c4c103e-48e8-44fa-817f-13de6a3d101c)


## The xgboost alogrithm performance was enhanced by changing the split to 0.2, increasing the depth of the tree to 50, and the number of estimators to 100.
