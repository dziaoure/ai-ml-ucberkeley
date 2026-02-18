# From Data to Intervention: Predicting Student Dropout Risk Using Machine Learning

## Project Overview

This project applies machine learning to predict student dropout risk using demographic, academic, and institutional data from the **"UCI Predict Students’ Dropout and Academic Success"** dataset.

The goal is not just prediction, but early identification — enabling targeted intervention before students leave the institution.

## Project Structure

### 1. Business Understanding

#### Research Question:
Can we predict which students are at risk of dropping out using demographic and first-semester academic data?

#### Objective:
Develop a predictive baseline model that supports early intervention strategies.


### 2. Data Understanding

- Dataset: UCI Machine Learning Repository
- 4,424 student records
- Demographic, academic, financial, and institutional variables
- Initial EDA to explore distributions, class balance, and key patterns


### 3. Data Preparation

The following steps were performed during the data preparation phase.

- Second-semester variables were removed to prevent data leakage
- Column names were standardized
- Categorical features were converted to their most appropriate type
- The target variable was collapsed into two binary classes:
    - Dropout → 1
    - Non-dropout → 0
- Additional minimal, hypothesis-driven features were engineered:
    - Approval rate (1st semester)
    - Evaluation participation rate
    - Financial risk flag
- A clean preprocessing pipeline was built using a ColumnTransformer


### 4. Data Modeling

The following steps were performed during the data modeling phase:
- The data was split into train and test sets using an **80/20** ratio
- A Logistic Regression model was used as a baseline model
- One-hot encoding was applied to categorical variables
- Standard scaling was applied to numeric variables


### 5. Evaluation
The following metrics show the performance of the baseline model on the test data:
- Accuracy: **86.78%**
- Precision: **86.46%**
- Recall: **69.72%**
- F1 Score: **0.7719**
- ROC-AUC: **0.9129**

The model demonstrates strong class separation (AUC > 0.90) while maintaining high precision and solid recall for the dropout class.

Future models will need to outperform those metrics to be considered better.


## Citations

### Data: 

Predict Students' Dropout and Academic Success

### URL
https://archive.ics.uci.edu/dataset/697/predict%2Bstudents%2Bdropout%2Band%2Bacademic%2Bsuccess

### Authors:
M.V.Martins, D. Tolledo, J. Machado, L. M.T. Baptista, V.Realinho. (2021) "Early prediction of student’s performance in higher education: a case study" Trends and Applications in Information Systems and Technologies, vol.1, in Advances in Intelligent Systems and Computing series. Springer. DOI: 10.1007/978-3-030-72657-7_16