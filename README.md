# cardiovascular-risk-prediction-project
### ***Project Summary*** 
Now a days, heart disease prediction has been a major concept in recent world that is impacting the society towards health. The main concept is to identify the age group and heart rate using the Random forest algorithm. Our project tells how the heart rate and condition is estimated based on the inputs such as blood pressure and many more being provided by the user to a system. This is being much better way when it comes with others algorithms the implementation of RFA gives the better experience and provide accurate result. This helps in early prediction of the disease and is used in many ways, where as it is being provided with the input, in order to find the heart rate based on the health condition.
### ***Problem Statement***
The classification goal is to predict whether the patient has a 10-year risk of future coronary heart disease (CHD).
### ***Approaches***
we will break this endeavor into different parts-:
### ***EDA***
- In this i have created different charts like Bar, Kde, Histogram, Box, Heatmap and Pair Plot for getting insights from the data and based on that we can do some feature Engineering.
- I also performed Hypothesis Testing based on our findings.
### ***Feature Engineering & Data Pre-processing***
- In this i Handled Missing Values, Outliers, Categorical Encoding.
- Performed Feature Manipulation to minimize feature correlation and create new features.
- Applied VIF to avoid avoid overfitting.
- ***Data Transformation*** i used log transformation to transform data because in some of the columns our data is positively skewed and for positively skewed lof transformation is used.

For predicting chd positive i used many ml algo like logistic regression,Random forest,KNN,SVC,Decision Tree,XGBOOST.
For untuned XGBOOST-:
For training dataset, i found accuracy 78% and for test dataset 72%.
For tuned XGBOOST-:
For training dataset i found acccuracy 99% and for test dataset 79%.
recall= 33%%
precision = 29%
Accuracy(Test) = 79% For testing dataset, i found precision of 89% and recall of 82% and f1-score of 86% for TenYearCHD Negative.And I got precision of 28% and recall of 41% and f1-score of 33% TenYearCHD Positive. Accuracy is 77%.
I would like to go with both Accuracy and recall.

Accuracy help us to detect overall TenYearCHD Positive.

In our model False Negative is important.

To reduce false negative recall is important. Again false negative defines as model will predict that the patient dont have TenYearCHD but the Patient really have TenYearCHD. That will be an issue for us. So, for that case we have to minimize the false negative. we must improve the score of recall.
I have choosen XGBoost model which is hyperparameter optimized. first of all I need accuracy thats why i choose Tuned XGBOOST.
In our case False Negative is also important, so if recall is more important then for that case use Random forest because Random forest gives higher recall.
I used SHAP Values(shapley Additive explanations) is a method based on cooperative game theory.

It gives contribution of each feature value to the prediction for a given instance.

In the summary plot we can see the top 12 columns and their impact on the prediction. The red color indicates that the value of the columns is high and blue color shows that the value of the column is low.

For categorical columns, we have zeros and ones where zero is blue color and one is red color.

Shap values are also displayed and the impact on the prediction is also shown. towards the right hand side, the impact is positive (increases the predicted value) and towards the left hand side, the impace is negative (decreases the predicted value).
In conclusion, this project demonstrated the potential of machine learning techniques to accurately predict the 10-year risk of future coronary heart disease (CHD) in patients using data from an ongoing cardiovascular study. Key points from this project include:

Careful data preprocessing and transformation improved the performance of machine learning models and enabled more accurate predictions.

Feature selection was important for identifying the most relevant predictors of CHD risk.

The XGBOOST (tuned) was chosen as the final prediction model due to its high accuracy score.

The XGBOOST (untuned) was chosen as the final prediction model due to its high recall score.
Techniques such as SMOTE were used to handle imbalanced data and improve model performance.

This project provides a valuable example of how machine learning techniques can be applied to real-world problems to achieve positive business impact.
