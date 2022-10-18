# Cardiovascular-Disease-Classification-project
## WE HAVE USED CARDIOVASCULAR DISEASE DATASET. BASED ON SOME HEALTH INFORMATION OF AN INDIVIDUAL OUR MODEL WILL PREDICT WHETHER HE HAS ANY CARDIOVASCULAR DISEASE OR NOT.

### DATA DESCRIPTION
There are 3 types of input features:
1. Objective: factual information;
2. Examination: results of medical examination;
3. Subjective: information given by the patient.

### FEATURES:
- Age | Objective Feature | age | int (days)
- Height | Objective Feature | height | int (cm) |
- Weight | Objective Feature | weight | float (kg) |
- Gender | Objective Feature | gender | categorical code |
- Systolic blood pressure | Examination Feature | ap_hi | int |
- Diastolic blood pressure | Examination Feature | ap_lo | int |
- Cholesterol | Examination Feature | cholesterol | 1: normal, 2: above normal, 3: well above normal |
- Glucose | Examination Feature | gluc | 1: normal, 2: above normal, 3: well above normal |
- Smoking | Subjective Feature | smoke | binary |
- Alcohol intake | Subjective Feature | alco | binary |
- Physical activity | Subjective Feature | active | binary |
- Presence or absence of cardiovascular disease | Target Variable | cardio | binary |

### PREPROCESSING NEEDED
- ID needs to be dropped.
- Age provided is in days. We will convert it to years
- Gender can be converted to binary
- ap_hi and ap_lo has negative numbers. This means that we have outliers so we need to remove them.
- Gluc and Cholesterol need to be converted to dummies
- There are many rare cases in height and weight features, so we can combine them in BMI feature (get 1 
feature from 2 features)

### DATA CLEANING & PREPROCESSING
- Remove Outliers
    - BMI more than 100 or less than 10
    - ap_hi more than 250 or less than 20
    - ap_lo more than 200 or less than 20
- Convert categorical variable into indicator variables
- Scaling non-categorical data
- PCA

### TRAINING
Splitting data into 0.25% for testing and 0.75% for training

### CLASSIFICATION
We used different classifiers and used accuracy and F1 score to evaluate the classifiers

_Classifiers Used:_

1. Logistic Regression 
2. Decision Tree 
3. Random Forrest 
4. Support Vector Machine
5. K-Nearest Neighbor
6. Naïve Bayes 
