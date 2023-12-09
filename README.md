# CIND820-Capstone-Heart-Disease-Prediction

### Introduction to Project

Cardiovascular diseases (CVDs) are the leading cause of death globally and are among the most prevalent chronic diseases in the United States, leading to 1 in 5 deaths annually. The term “heart disease” or CVD can refer to several types of heart conditions, with the most common type being coronary artery disease (CAD). Eventually, most of theses heart diseases will lead to a myocardial infarction (heart attack) or a stroke. It is paramount that timely, effective and precise intervention be taken to ensure that patients are diagnosed and treated properly. In this respect, machine learning (ML) algorithms and approaches can help in the classification and prediction of heart diseases by looking at patient history, chronic diseases and past behaviours, as sometimes heart disease is not diagnosed until an individual experiences the symptoms of heart failure. 

Machine learning algorithms can be used to assess behavioural risk factors for heart disease, the most important of which are: unhealthy diet, physical inactivity, smoking, high alcohol consumption, high cholesterol, hypertension, and obesity, among other things. Identifying those at the highest risk of heart failure and disease can lead to ensuring they receive proper treatment and prevent their premature deaths. The effectiveness of multiple different ML models, including Logistic Regression, K-Nearest Neighbors (KNN), Support Vector Machines (SVM), Random Forests, and XGBoost in the classification and prediction of heart disease was analyzed and compared. 

The objective was to assess which model would be the most accurate and appropriate, therefore improving detection methods and preventing negative outcomes. Additionally, the features most useful in predicting heart disease were also outlined for preventative health screening. Risk factors most associated with and most predicative of heart disease and fatality, as well as which subset of risk factors may be used to accurately predict whether an individual has heart disease or not.

The data used in this study was an open dataset from 2019 conducted by the Centre of Disease Control and Prevention’s (CDC) annual Behavioral Risk Factor Surveillance System (BRFSS), available from [https://www.cdc.gov/brfss/annual_data/annual_2019.html]. It consisted of 418,268 individuals and had 343 features. The dataset was cleaned, and features were selected according to relevance, including but not limited to, high blood pressure, high cholesterol, body mass index (BMI), smoker, stroke, diabetes, and physical activity and more. The working dataset had 256203 responses and 18 features. Exploratory data analysis was applied to the dataset to understand relationships, correlations and distributions in Python, using python libraries such as pandas, NumPy, matplotlib, seaborn and scikit. Cross validation was performed on all models. Imbalanced target variable was also handled using random under samlping and SMOTE. The dataset was split into train and test sets for each of the following models: Logistic Regression, Random Forests, Support Vector Machines, K-Nearest Neighbors and XGBoost. Each model was evaluated for its accuracy, precision, recall and F1 score, as well as fit time. 


### Tentative Stages of the Project
1. Project proposal: This phase of the project revolves around finding a public and open dataset and seeing if it might be a valid and viable option to meet the projects requirements.
2. Cleaning the dataset: This phase involves cleaning the dataset so that it may be used. This includes handling all outliers, missing values, and standardizing the variables so that the data may be used for analysis and model creation.
3. Initial Analysis and Literature Review: After the dataset has been cleaned and is ready to be used, initial analysis will be performed to see the distribution of features, the correlation between features and size and shape of the dataset. A comprehensive literature review should also be carried out to see how past researchers have employed techinques and answered research questions related to similar or same data. This will be a good guideline in model selection and will also allow us to understand why our project is important as a contribution.
4. Exploratory Data Analysis: After the data has been cleaned, initial analysis has been performed and past research has been considered, exploratory data analysis may proceed. This outlines the general trends in the data, as well as correlation between the target variable and correlation between other variables. This is more in depth than the initial analysis and gives us an insight into how our dataset functions and what inferrances we can make from it. This will also help us with feature selection for our models.
5. Feature selection and handling imbalanced data (if any): Before we can begin with our model, feature selection must be performed to see which features we will include in our final models or not. After the features have been selected (either removed or kept in the dataset), we can begin handling our imbalanced data (if there is any). This can involve multiple things, such as splitting the dataset into a train/test split and then performing either oversampling or undersampling (or both) on the TRAIN set only, so that our test set can be used as a reliable real world example of our models.
6. Creating the models and feature importance: The literature review helped us choose which models would be most approraite for our dataset, and feature selection and imbalanced data will help us have a model that can be as accurate as possible to the best our abilities. Each model will be cross validated and performance metrics will be recorded, as well as the fit times. Features that were most important in the models will also be recoreded.
7. Model Comparision: Comparing our models to see which was the overall most effective, taking into account both model performance and model fit time.
8. Final Report: A final report compiling, revising and aggregating all the above stages into one file.
9. Final Presentation: Condensing the most vital aspects of the final report into a presentation that can be interpreted and understood by stakeholders.


 ### File Legend
 1. heart_disease_brfss2019.csv --> The cleaned dataset
 2. brfss2019_cleaning_data.ipynb --> the notebook used to clean the dataset
 3. brfss2019_heart_disease_initial analysis.ipynb --> the initial analysis of the dataset. This notebook also includes attribute information and project goals
 4. brfss_EDA_heart_disease.ipynb --> exploratory data analysis notebook
 5. brfss_ML_models_heart_disease.ipynb --> notebook comprising of feature selection, handling imbalanced target variable, creating machine learning models, feature importance, and finally model comparisions. This file gives insight into how well the models performed and important features in classification.

### Results
| Model | Accuracy | Precision | Recall | F1-Score | Fit Time |
| ----- | -------- | --------- | ------ | -------- | -------- |
| Logistic Regression | 79.2% | 27.9% | 67.3% | 0.394 | 0.14s |
| K-Nearest Neighbors | 78.8% | 26.9 | 64.7% | 0.380 | 0.08s |
| Support Vector Classifier | 78.0% | 27.0% | 69.9% | 0.390 | 40.5s |
| Random Forests | 78.4% | 27.5% | 70.2% | 0.395 | 7.29s |
| XGBoost | 77.9% | 27.1% | 71.2% | 0.393 | 0.11s |


Overall, considering the accuracy, the F1-score, the trade off between precision/recall (recall is slightly more important for this specific dataset), and the fit times, the preferred model would be XGBoost. It was the second quickest model to fit at 0.11s and had a high F1-score at 0.393. The recall was also the highest of all the models at 0.71. The accuracy, despite being the lowest was still good at 77.9%. However, it should be noted that if model fit times are not a problem and the infrastructure to run complex algorithms is available, then the preferred model would have to be random forest classifier, which had the overall best metrics with high recall, f1-score, and accuracy.  


In terms of feature importance, both random forests and XGBoost were quite similar, with the top four and bottom four features being the same across both models. High blood pressure, general health, age, and high cholesterol seem to be the most important factors in classification of heart disease. Diabetes, Stroke and Sex also play a role to some degree but not as much as the former features. Income seems to have least affect on determining and classifying heart disease and this was true for both random forest classifier importance and XGBoost importance. In a clinical setting, with some form of health expert or researcher surveying patients or individuals, the most important features to focus on the in the dataset would be age, followed closely by high blood pressure and high cholesterol. General health should also have a significant impact in screening, as it affects multiple areas of life such as physical activity and diet. Sex, previous history of stroke and diabetes should also be important factors to consider.

