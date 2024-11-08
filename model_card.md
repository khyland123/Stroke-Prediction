# Model Card

## Model Description

**Input:** 

The input variables were 
gender: "Male", "Female" or "Other"
age: age of the patient
hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
ever_married: "No" or "Yes"
work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
Residence_type: "Rural" or "Urban"
avg_glucose_level: average glucose level in blood
bmi: body mass index
smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*


**Output:**
The output variable is stroke

**Model Architecture:** 
Logistic regression was selected because it outperformed decision tree, random forest and a SVM model.

## Performance

The performance metrics are given below:

Model: Logistic Regression
              precision    recall  f1-score   support

           0       0.99      0.71      0.83      1203
           1       0.15      0.82      0.26        74

    accuracy                           0.72      1277
   macro avg       0.57      0.77      0.54      1277
weighted avg       0.94      0.72      0.80      1277

