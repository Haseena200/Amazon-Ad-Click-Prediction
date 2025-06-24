# Amazon-Ad-Click-Prediction
•	This project focuses on predicting whether a user will click on an online advertisement using machine learning. By analyzing user demographics, browsing behavior, device type, ad position, and time of day, a binary classification model was trained to identify patterns in user engagement. The model helps improve ad targeting and optimize marketing strategies for better click-through rates.
## Aim
•	To develop a machine learning model that can predict whether a user will click on an online advertisement based on their demographic information, browsing behavior, and the contextual display of the ad.
## Solution Approach
1. Exploratory Data Analysis (EDA)
 - Data Inspection: Checked for missing values, data types, and imbalance in the target column (click).
  - Target Distribution: Found that the click behavior was imbalanced (more 0s than 1s).
  - Univariate Analysis: Visualized individual features such as age, gender, and device_type using histograms and bar plots.
  - Bivariate Analysis: Explored relationships between input features and the click target using group-wise comparisons.
  - Outlier Detection: Detected outliers in age using boxplots.
    Insights Gained:
  - Younger users clicked more frequently.
  - Mobile users were more likely to click ads compared to Desktop and Tablet users.
2. Data Preprocessing
   -  Dropped Irrelevant Column: full_name was removed as it had no predictive use.
   -  Label Encoding: Categorical variables (gender, device_type, ad_position, browsing_history, time_of_day) were encoded using LabelEncoder.
   -  Missing Values:
   - Categorical features filled with 'Missing'.
   - Numerical features (age) filled with median.
   - Feature Selection: Removed columns like id during model training, and handled necessary feature engineering steps.
    3. Model Building
   - Problem Type: Binary classification (predicting click = 1 or 0).
    -    Models Tested:
    
    Logistic Regression (suggested in description)
    
    Decision Tree Classifier
    
    Random Forest (final chosen model for its robustness)
    
    (Optional) Hyperparameter Tuning:

Techniques like GridSearchCV or RandomizedSearchCV can be used to tune:

n_estimators, max_depth, min_samples_split

Note: This is suggested, but not included in your current code.

4. Model Evaluation
Metrics Used:

Accuracy: Overall performance

Precision & Recall: Important due to class imbalance

F1-Score: Balanced metric for binary classification

Confusion Matrix: Detailed performance analysis

ROC-AUC: Optional but useful for visual threshold analysis (not implemented in current code)

5. Final Prediction
Predictions made on test.csv using the trained model.

Results saved to submission.csv in the format: id, click.
