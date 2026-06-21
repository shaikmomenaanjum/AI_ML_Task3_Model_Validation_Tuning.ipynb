# AI_ML_Task3_Model_Validation_Tuning.ipynb
Machine Learning project focused on overfitting control, model validation, and hyperparameter tuning for house price prediction.
MODEL VALIDATION, OVERFITTING CONTROL & HYPERPARAMETER TUNING

Submitted By: Momena Anjum

INTRODUCTION

This project focuses on improving the performance of a house price prediction model by applying model validation and optimization techniques. The California Housing dataset was used to evaluate model behavior, identify overfitting, and improve prediction accuracy through hyperparameter tuning.
The main goal of this task was to build a model that performs well not only on training data but also on unseen test data. To achieve this, Cross-Validation and GridSearchCV were used during the model development process.

METHODOLOGY
The California Housing dataset was prepared by separating the feature variables and the target variable. StandardScaler was applied to normalize the data before model training. The dataset was then split into training and testing sets.

Training Data: 16,512 samples

Testing Data: 4,128 samples

A Decision Tree Regressor was first trained without limiting its depth. The model achieved a Train RMSE of 0.0000 and a Test RMSE of 0.7030. This indicated that the model was overfitting because it learned the training data perfectly but struggled when predicting new data.
To evaluate performance more reliably, 5-Fold Cross Validation was performed. The model achieved a Cross-Validation RMSE of 0.8957.
Hyperparameter tuning was then carried out using GridSearchCV. Different values of max_depth and min_samples_split were tested automatically to identify the best model configuration.

Best Parameters:

max_depth = 10

min_samples_split = 10

RESULTS AND DISCUSSION

The final tuned model was compared with Linear Regression and Ridge Regression.

Linear Regression:
RMSE = 0.7456
R² Score = 0.5758

Ridge Regression:
RMSE = 0.7456
R² Score = 0.5758

Tuned Decision Tree:
RMSE = 0.6454
R² Score = 0.6821

The Tuned Decision Tree achieved the strongest performance among all tested models. It generated lower prediction errors and explained a larger portion of the variation in house prices. The results clearly show that model tuning can significantly improve prediction quality compared to using default settings.
CONCLUSION

This project demonstrated the importance of overfitting detection, Cross-Validation, and Hyperparameter Tuning in Machine Learning. The optimized Decision Tree model outperformed both Linear Regression and Ridge Regression by achieving the lowest RMSE and highest R² score.
The final model provided more reliable predictions and better generalization to unseen data. Future improvements could involve testing advanced ensemble methods such as Random Forest Regression and Gradient Boosting to further enhance performance.
