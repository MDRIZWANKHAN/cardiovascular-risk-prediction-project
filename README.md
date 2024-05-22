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
- ***Data Scaling*** I used MinMaxScaler.
- MinMaxScaler is a popular feature scaling technique used to transform numerical features to a common scale. It scales the features to a fixed range (usually between 0 and 1) based on the minimum and maximum values of the features.
- ***Data Splitting*** I used 80:20 data splitting ratio.
- When we split our data into training and test sets, we're essentially creating two different datasets that we can use to test our model's performance. This can help us identify any issues with our data, such as outliers or missing values, and make our model more robust to these issues.
### ***ML Model Implementation***
***ML Model - 1- Implementing Logistic Regression***
 - I used Logistic regression algorithm to create the model. As I got not so good result.
 - For testing dataset, i found precision of 93% and recall of 64% and f1-score of 76% for TenYearCHD negative.And I got precision of 24% and recall of 69% and f1-score of 36% for TenYearCHD Positive,and Accuracy is 65%.
 - Now,tryting to improving the score by using hyperparameter tuning technique.I used GridSearchCV it appears that hyperparameter tuning did not improve the performance of the Logistic Regression model on the test set.
   
***ML Model - 2- RandomForestClassifier***
 - For training dataset, i found precision of 98% and recall of 94% and f1-score of 96% for TenYearCHD Negative.And I got precision of 94% and recall of 98% and f1-score of 96% for TenYearCHD Positive. Accuracy is 96%.
 - For testing dataset, i found precision of 89% and recall of 82% and f1-score of 86% for TenYearCHD Negative.And I got precision of 28% and recall of 41% and f1-score of 33% TenYearCHD Positive. Accuracy is 77%.
 - For training dataset, i found precision of 98% and recall of 94% and f1-score of 96% for TenYearCHD Negative.And I got precision of 94% and recall of 98% and f1-score of 96% for TenYearCHD Positive. Accuracy is 96%.
 - ***Implemented KNeighborsClassifier,KNeighborsClassifier*** but did not get good result.
 - Finally got ***good result*** on ***XGBOOSTClassifier***
 - For ***untuned XGBOOST***-:
      - For training dataset, i found accuracy 78% and for test dataset 72%.
      - recall for test is 61%
 - For ***tuned XGBOOST***-:
      - For training dataset i found acccuracy 99% and for test dataset 79%.
      - recall= 33%%
      - precision = 29%

- I used ***SHAP Values(shapley Additive explanations)*** method to find feature importance.
  
### ***Conclusion***
In conclusion, this project demonstrated the potential of machine learning techniques to accurately predict the 10-year risk of future coronary heart disease (CHD) in patients using data from an ongoing cardiovascular study. Key points from this project include:

- Careful data preprocessing and transformation improved the performance of machine learning models and enabled more accurate predictions.
- Feature selection was important for identifying the most relevant predictors of CHD risk.
- The XGBOOST (tuned) was chosen as the final prediction model due to its high accuracy score.
- The Logistic Regression(untuned) was chosen as the final prediction model due to its high Recall score.
- Techniques such as SMOTE were used to handle imbalanced data and improve model performance.
- This project provides a valuable example of how machine learning techniques can be applied to real-world problems to achieve
  positive business impact.
Overall, this project highlights the importance of careful data preparation and analysis in machine learning projects.
  By taking the time to clean and transform the data, select relevant features, and choose an appropriate model,
  it is possible to achieve accurate predictions and support decision-making in a wide range of domains.
