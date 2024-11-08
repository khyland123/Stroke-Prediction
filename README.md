# Stroke Prediction


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
This project aims to determine which features are predictive of stroke. Stroke is one of the leading causes of death and long-term disability worldwide. Prompt identification and intervention can significantly reduce the severe outcomes, including paralysis, speech difficulties and even death. According to the WHO, 15 million people worldwide have a stroke each year, with 5 million dying and 5 million becoming permanently disabled.

Predicting stroke risk can help identify individuals who would benefit from preventative measures, such as lifestyle changes and medications. High risk individuals can be monitored more closely.

## DATA
The stroke dataset from Kaggle (https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) includes a patient id, 10 features and an outcome variable for stroke. Details about each variable in the dataset are presented below:
1) id: unique identifier
2) gender: "Male", "Female" or "Other"
3) age: age of the patient
4) hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5) heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6) ever_married: "No" or "Yes"
7) work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8) Residence_type: "Rural" or "Urban"
9) avg_glucose_level: average glucose level in blood
10) bmi: body mass index
11) smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12) stroke: 1 if the patient had a stroke or 0 if not
*Note: "Unknown" in smoking_status means that the information is unavailable for this patient

The source of this dataset is not explicitly stated on Kaggle and the dataset is to be used for educational purposes only. The author can be contacted if this dataset is to be used in research. The dataset is well documented and well maintained. There are some missing observations for BMI but other than that the dataset is clean.

Of the 5110 participants included in this dataset, 687 were children (work_type=children) and of those individuals, 2 had a stroke. Including participants under the age of 18 seems to be uninformative for this analysis. I would advise researchers to aim to identify more children who had experienced a stroke in order to improve the ability of the model to predict stroke in children. As a result of this, children under 18 years of age were removed from the analysis.

## MODEL 
The frequency of stroke cases were significantly underrepresented in this dataset and oversampling was used on the training dataset to improve the performance of the model in predicting stroke.

Various models were used for this analysis, including logistic regression, decision tree, random forest and support vector machine. The models generally had similar performance but the logistic regression model was selected because its precision in predicting actual stroke cases was slightly higher than the other models.

## RESULTS
The main features that were predictive of stroke in adults were age, average glucose level, BMI, hypertension, heart disease, work type being private and smoking status of having never smoked

In particular, being older, high average glucose level, high BMI, having hypertension, having heart disease and working in the private sector increase the risk of stroke in adults and having never smoked reduces the risk of stroke in adults.

