# Amazon-Ad-Click-Prediction
•	This project focuses on predicting whether a user will click on an online advertisement using machine learning. By analyzing user demographics, browsing behavior, device type, ad position, and time of day, a binary classification model was trained to identify patterns in user engagement. The model helps improve ad targeting and optimize marketing strategies for better click-through rates.
## Aim
•	To develop a machine learning model that can predict whether a user will click on an online advertisement based on their demographic information, browsing behavior, and the contextual display of the ad.
## Solution Approach
1.	Exploratory Data Analysis (EDA)
 -	Data Inspection: Checked for missing values, datatypes, and class imbalance in the target (click) column.
 - Target Distribution: Found that click behavior was imbalanced (more 0s than 1s).
 -	Univariate Analysis: Visualized individual features like age, gender, and device_type using histograms and bar plots.
 - Bivariate Analysis: Analyzed relationships between features and click using heatmaps and group comparisons.
 - 	Outlier Detection: Identified unusual values in age via boxplots. Insights:
 -	Younger users clicked more often.
 - Mobile users were more likely to click ads than desktop or tablet users.
2.	Data Preprocessing
-	Dropped Irrelevant Columns: full_name was removed due to no predictive value.
-	Label Encoding: Categorical variables (gender, device_type, ad_position, etc.) were encoded using LabelEncoder.
-	Handled Missing Values: Filled missing values using mode (categorical) and median (numerical).
- Feature Selection: Removed unnecessary or highly correlated columns.
3.	Model Building
-	Problem Type: Binary Classification – Predicting click (0 or 1).
-	Models Tested:
-	Logistic Regression
-	Decision Tree
-	Random Forest (Primary Model) – chosen for handling mixed data types and avoiding overfitting.
-	Hyperparameter Tuning: Used GridSearchCV / RandomizedSearchCV to optimize:
-	n_estimators, max_depth, min_samples_split
-	Outcome: Improved accuracy and F1-score with tuned Random Forest model.
4.	Model Evaluation
-	Metrics Used:
-	Accuracy – overall correctness
-	Precision & Recall – for handling imbalance
-	F1-Score – key metric due to class imbalance
-	Confusion Matrix – performance summary
- ROC-AUC Curve – assessed model's classification threshold
5.	Final Prediction
-	Predictions made on test.csv
-	Results saved in submission.csv
