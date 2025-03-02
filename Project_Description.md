# Group_Project
Group Project for INSY - 695 Adv Topics in IS 1 ( ML in Production)

![image](https://github.com/user-attachments/assets/58e8a733-4da5-448a-9a86-985ea1f2f786)

Importing the Dataset from the APIs


![image](https://github.com/user-attachments/assets/a1599d04-0494-49f1-a74b-58b9823f8fab)

Merging the datasets

**EDA** | **DATA PREPROCESSING** | **FEATURE ENGINEERING** |

![image](https://github.com/user-attachments/assets/e389c01f-ddfb-4ef4-8d83-1bc945d2ec75)


![image](https://github.com/user-attachments/assets/7b43d889-9c60-4ec8-bf8a-1805aa5b4277)


![image](https://github.com/user-attachments/assets/ecb85136-4fca-4f8a-ae6f-74d39bee5a01)


![image](https://github.com/user-attachments/assets/fe9ef5e4-9bff-487b-adf8-ba6d89358ab1)


![image](https://github.com/user-attachments/assets/a7e4c08a-e353-4e9d-ad5c-82273e93a19a)



![image](https://github.com/user-attachments/assets/8321c635-eb94-4fdc-a534-4d98edeca6a0)



**Exploratory Data Analysis (EDA)**-->

a. Initial Data Inspection

Summary Statistics:

– Use methods like .describe() to view mean, median, standard deviation, etc.

– Identify the range and distribution of numeric features.

Missing Values & Duplicates:

– Visualize missingness (using heatmaps or missingno library).

– Handle duplicates if present.

b. Univariate Analysis

Numeric Variables:

– Histograms and boxplots to understand the distributions and detect outliers.

Categorical Variables:

– Bar charts to display frequency counts.



![image](https://github.com/user-attachments/assets/fcc25081-81bd-402e-8dc5-5afe28106c62)



![image](https://github.com/user-attachments/assets/75f1f7b4-4273-4951-adc4-25a723c94a57)



![image](https://github.com/user-attachments/assets/596df875-ba49-44f3-9e57-cabb60c9aa3d)


![image](https://github.com/user-attachments/assets/e6300ca6-b187-42ea-94bc-dee250d77ca3)


**Data Cleaning & Transformation**

Missing Data Imputation:
– For numeric features, considered median/mean imputation or advanced methods (e.g., KNN imputation).

– For categorical features, imputed with the mode, frequency also did the imputation using the a model randomforestclassifier to impute values

Outlier Treatment:

– Winsorize or cap extreme values

Did Label Encoding aswell 

**Supervised Learning: Predicting outcome_type**

a. Model Selection & SOTA Methods

Candidate Models:

– Gradient Boosting Machines: e.g., XGBoost, LightGBM

– Ensemble Models: Random Forest or stacking multiple models.

– Neural Networks: MLP Classifier

**Model Training & Validation**

Data Splitting:

– Used stratified k-fold cross-validation to ensure that class proportions are maintained in each fold.

Hyperparameter Tuning:

– Used grid search

Evaluation Metric:

– Used AUC-ROC as the primary metric. Ploted ROC curves for each model to compare performance.
Did
