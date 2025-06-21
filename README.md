# Description:
This repository contains the code and resources for a machine learning project aimed at predicting whether a user will click on an Amazon advertisement based on user behavior and profile features logged in ad server data.

## Project Aim
To build a machine learning classification model that predicts whether a user will click on an Amazon advertisement. The model leverages user demographic and behavioral data from ad server logs to support data-driven advertising strategies and improve targeting effectiveness.

## Dataset Used
train.csv
test.csv

## Solution Approach
1. Data Preprocessing
- Removed irrelevant columns (e.g., full_name)
- Checked for null values and handled them (if any)
- Encoded categorical variables (LabelEncoding / OneHotEncoding)
- Split train.csv into features (X) and target (y)
2. Exploratory Data Analysis (EDA)
- Visualized class imbalance
- Analyzed trends based on:
- Age groups and click behavior
- Gender vs click
- Device type vs click
- Ad position influence
- Time of day vs user activity
3. Model Building
- Tried multiple classification algorithms
- Used train_test_split for validation
- Evaluated using:
. Accuracy
.  Precision
. Recall
. F1-score
. Confusion Matrix
4. Prediction & Submission
- Selected the best performing model
- Applied the model on test.csv
- Created submission.csv with final predictions

## Key Questions Answered
- What percentage of users clicked on ads in the dataset?
- Which features most influence ad click behavior?
- How well can we predict future user interactions?
- What’s the performance of the Random Forest model?
- Can we identify high-probability click users?

## Key Insights
- Top Predictors: Age, device type, and timestamp contribute most to predicting ad clicks.
- Model Performance: Random Forest achieved good accuracy with balanced precision and recall.
- Engagement Patterns: Certain demographics show higher click-through rates.
- Business Impact: Better targeting of ads to high-engagement users.

## Final Conclusion 
This machine learning project demonstrates the potential of using user data to predict ad click behavior. The model achieved strong performance and offers actionable insights for improving ad targeting. With further tuning and real-time integration, this solution can significantly enhance the efficiency of advertising campaigns.
