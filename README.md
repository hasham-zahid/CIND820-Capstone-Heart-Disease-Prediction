# CIND820-Capstone-Heart-Disease-Prediction

 ### File Legend
 1. heart_disease_brfss2019.csv: The cleaned dataset
 2. Data_Cleaning_Transforming_brfss2019.ipynb: The notebook used for data wrangling; to clean and transform the dataset
 4. Exploratory_Data_Analysis_brfss2019.ipynb: Exploratory data analysis, visulizations, insights into the data notebook
 5. Predictive_Models_and_Results_brfss2019.ipynb: Notebook comprising of feature selection, handling imbalanced target variable, creating machine learning models, feature importance, and finally model comparisions. This file gives insight into how well the models performed and important features in classification.
 6. brfss2019_Final_Report.pdf: This includes the cumalative final report, including but not limited to the literature review, exploratory data analysis, handling of imbalanced data, predictive models and features, shortcomings, strengths, contributions and challenges and further work. This offers more of an indepth understanding of the project and its phases. 

### Table of Contents
1. Introduction to the Project and Cardiovascular Disease
2. Dataset Information
3. Tentative Stages of the Project
4. Overall Methodology and Approach
5. Insights About The Dataset
6. Handling Imbalanced Data and Feature Selection
7. Results for Predictive Models
8. Results for Feature Importance
9. Conclusions and Further Work

### Introduction to the Project and Cardiovascular Disease
Cardiovascular diseases (CVDs) are the leading cause of death globally and are among the most prevalent chronic diseases in the United States, leading to 1 in 5 deaths annually. The term “heart disease” or CVD can refer to several types of heart conditions, with the most common type being coronary artery disease (CAD). Eventually, most of theses heart diseases will lead to a myocardial infarction (heart attack) or a stroke. It is paramount that timely, effective, and precise intervention be taken to ensure that patients are diagnosed and treated properly. In this respect, machine learning (ML) algorithms and approaches can help in the classification and prediction of heart diseases by looking at patient history, chronic diseases, and past behaviours, as sometimes heart disease is not diagnosed until an individual experiences the symptoms of heart failure.

Machine learning algorithms can be used to assess behavioural risk factors for heart disease, the most important of which are: unhealthy diet, physical inactivity, smoking, high alcohol consumption, high cholesterol, hypertension, and obesity, among other things. Identifying those at the highest risk of heart failure and disease can lead to ensuring they receive proper treatment and prevent their premature deaths. The effectiveness of multiple different ML models, including Logistic Regression, K-Nearest Neighbors (KNN), Support Vector Machines (SVM), Random Forests, and XGBoost in the classification and prediction of heart disease was analyzed and compared.

The objective was to assess which model would be the most accurate and appropriate, therefore improving detection methods and preventing negative outcomes. Additionally, the features most useful in predicting heart disease were also outlined for preventative health screening of risk factors. This would give insight into the most associated with and most predicative risk factors of heart disease and fatality, as well as which subset of risk factors may be used to accurately predict whether an individual has heart disease or not.

The data used in this study was an open dataset from 2019 conducted by the Centre of Disease Control and Prevention’s (CDC) annual Behavioral Risk Factor Surveillance System (BRFSS), available from [https://www.cdc.gov/brfss/annual_data/annual_2019.html]. It consisted of 418,268 individuals and had 343 features. The dataset was cleaned and transformed, and features were selected according to relevance, including but not limited to, high blood pressure, high cholesterol, body mass index (BMI), smoker, stroke, diabetes, and physical activity and more. The working dataset had 256203 responses and 18 features. Exploratory data analysis was applied to the dataset to understand relationships, correlations, and distributions in Python, using python libraries such as pandas, NumPy, matplotlib, seaborn and scikit. Cross validation was performed on all models and randomized search was used to find the best parameters for the model. Imbalanced target variable was also handled using random under sampling and SMOTE. The dataset was split into train and test sets for each of the following models: Logistic Regression, Random Forests, Support Vector Machines, K-Nearest Neighbors and XGBoost. Each model was evaluated for its accuracy, precision, recall and F1 score, as well as fit time.

### Dataset Information
The Behavioral Risk Factor Surveillance System (BRFSS) is a project conducted by the Centre for Disease Control and Prevention (CDC) in all states in the United States. This dataset is done via survey over the phone, and collects data on health risk behaviours, chronic diseases and conditions, access to healthcare and much more. The raw dataset was cleaned and only 18 attributes that would be relevant to heart disease prediction and classification were selected, such as specific demographics, health indicators, risk factors, and general health and wellness. The raw data was the 2019 BRFSS and consisted of 418,268 individuals and had 343 features. The dataset was cleaned and transformed, and features were selected according to relevance. The working dataset had 256203 responses and 18 features.

According to the CDC, important risk factors for heart disease are high blood pressure, high cholesterol, diabetes, smoking, obesity, unhealthy diet, and physical inactivity. From the 343 variables in the dataset, the health indicators in this dataset were chosen from this information. The attributes are split into different categories, such as demographics, clinical risk factors, and general health and wellness. The features of the dataset are the target variable, heart disease, age, sex, income, education, high cholesterol, high blood pressure, BMI (obesity), alcohol consumption, smoking, vegetables in diet, fruits in diet, diabetes, physical activity, stroke, general health, mental health and physical health. 

Raw dataset available from: [https://www.cdc.gov/brfss/annual_data/annual_2019.html]. The cleaned dataset can be found in the respository, as well as the notebook used to clean it.

### Tentative Stages of the Project
1. Project proposal: This phase of the project revolves around finding a public and open dataset and seeing if it might be a valid and viable option to meet the projects requirements.
2. Data Wrangling: This phase involves cleaning and transforming the dataset so that it may be used. This includes handling all outliers, missing values, and standardizing the variables so that the data may be used for analysis and model creation.
3. Initial Analysis of Variables: After the dataset has been cleaned and is ready to be used, initial analysis will be performed to see the distribution of features, the correlation between features and size and shape of the dataset 
4. Literature Review:  A comprehensive literature review should also be carried out to see how past researchers have employed techinques and answered research questions related to similar or same data. This will be a good guideline in model selection and will also allow us to understand why our project is important as a contribution.
5. Exploratory Data Analysis: After the data has been cleaned, initial analysis has been performed and past research has been considered, exploratory data analysis may proceed. This outlines the general trends in the data, as well as correlation between the target variable and correlation between other variables. This is more in depth than the initial analysis and gives us an insight into how our dataset functions and what inferrances we can make from it. This will also help us with feature selection for our models.
6. Feature selection and handling imbalanced data (if any): Before we can begin with our model, feature selection must be performed to see which features we will include in our final models or not. After the features have been selected (either removed or kept in the dataset), we can begin handling our imbalanced data (if there is any). This can involve multiple things, such as splitting the dataset into a train/test split and then performing either oversampling or undersampling (or both) on the TRAIN set only, so that our test set can be used as a reliable real world example of our models.
7. Creating the models and feature importance: The literature review helped us choose which models would be most approraite for our dataset, and feature selection and imbalanced data will help us have a model that can be as accurate as possible to the best our abilities. Each model will be cross validated and performance metrics will be recorded, as well as the fit times. Features that were most important in the models will also be recoreded.
8. Model Comparision: Comparing our models to see which was the overall most effective, taking into account both model performance and model fit time.
9. Final Report: A final report compiling, revising and aggregating all the above stages into one file.
10. Final Presentation: Condensing the most vital aspects of the final report into a presentation that can be interpreted and understood by stakeholders.

### Overall Methodology and Approach

The general goal of this project is to not only create a machine learning algorithm that is effective at predicting and classifying heart disease, but to compare the effectiveness of various machine learning algorithms with each other to determine which one would be the most accurate.  Additionally, a secondary objective to see which features and survey questions are more likely to be important in the prediction of heart disease compared to others was also determined (e.g., what features to look out for in patients).

Firstly, in the planning phase, research will be conducted in choosing the most relevant features of the dataset. The dataset will be cleaned, missing values handled, and outliers detected. The dataset will be made as consistent as possible. Initial analysis will be performed to determine the distributions of the attributes, especially the target variable, and the correlation of the attributes will be analysed. A literature review will also be conducted at this stage to determine which techniques to use and how similar studies have handled certain problems (e.g., imbalanced data).

Secondly, a more in-depth exploratory data analysis will be conducted on the dataset, and key takeaways from the data will be outlined. The data analysis will focus on the relationship between the target variable and other variables, as well as the relationship between non-target variables. Afterwards, the data will be balanced using SMOTE or RandomUndersampling and will be split into a train-test split. Features will be chosen, and a 5-fold cross validated randomized search will be performed on all models to find the best parameter. Randomized search was chosen over grid search to save computation time and complexity. 10-fold cross validation will then be used on the best parameters specifically to determine the stability of the model and the model will then be used on the test set to determine performance and fit time. 

Finally, the models will be trained and evaluated using accuracy, F1-score, precision and recall as the evaluation metrics. The techniques used will be Logistic Regression, K-Nearest Neighbors, Support Vector Machines, Random Forests, and XGBoost. In this phase, features that are most important in determining the correct output will also be analyzed using the Random Forests and XGBoost models, so they may act as general guideline in survey questions. 

###  Literature Review
The full literature review is long and covers multiple studies. For the sake of keeping this readme short, the full literature review can be found in the respository within the Final Report file. The purpose of the literature review was to analyze what past research and technqiues had been employed to similar problems and how challenges were overcome, giving an idea of how this project can be structured. This included information on which machine learning algorithms were employed, which technqiues were used to handle imbalanced data, information on the dataset and how this project can contribute further to the work. 

Addtionally, using the information acquired from the analyzing the literature, the objectives of this project can be reiterated. The purpose of this research paper is to analyze the effectiveness of different machine learning models in the prediction and detection of heart disease, as well as determine which general features would be most important in a survey from a healthcare expert in the determining of heart disease. The aforementioned studies are also attempting to do the same, with some of them focusing on different aspects or different techniques overall. For example, Plati et. al is the only study to focus on both the clinical aspect (surveys) and the technical aspect (machine learning models) with the research. Most of the studies mentioned only focus on the technical aspects.

Additionally, most of the studies were using the Cleveland Heart Disease dataset, which is a small dataset, and despite other studies using slightly larger datasets, they still lacked diversity. One of the main benefits of this dataset and project is that the variables are only behavioural and chronic risk factors (no electronic health records, ECG's, blood sample data, biomedical data, etc.). Therefore, we believe that this paper would be beneficial and worth doing due to focusing on a multitude of different aspects, such as mental health, specific demographics, physical health, diet, and clinical risks. Moreover, this paper also has a very large dataset consisting of over 250000 instances and 18 features. Although previous research is closely related to this paper, it is believed that this research would still be beneficial and of value in the diagnostic and screening of heart disease and may further help validate some of the previous findings with a larger dataset. 

### Insights About The Dataset
1. The percentage of people suffering from heart disease is far less than those who are not; imbalanced target variable
2. Despite being the minority class in the dataset, the proportion of males suffering from heart attack is higher than females. This may indicate that men are more at risk of heart disease than women.
3. As age increases, so does the risk of heart disease significantly.
4. High cholestrol seems to play a role in higher chance of heart disease.
5. High blood pressure also seems to affect risk of heart disease. 
6. Not a very significant link with BMI and heart disease found in the dataset, also further regurgitated by the correlation of BMI to heart disease
7. Despite being a small percentage of the entire dataset, people with diabetes made up a significant portion of all positive cases.
8. Stroke and heart disease seem to go hand in hand, as previous history of having a stroke does seem to increase likelihood of having CVD or MI. 
9. Income does not seem to play a huge factor in heart disease. Most of the individuals in the dataset made $75-80k/year. The increase from class to class in the income variable was mostly consistent, as was the risk of heart disease.
10. Mental health may play a small factor in heart disease (most likely due to increased stress). Individuals who described having poor mental health 30 days of the month did illicit more heart disease cases generally. However, overall it seems to have very little to do with increasing the risk of heart disease.
11. Individuals who described their general health to be poorer on average, generally had a higher proportion of positive cases of heart disease; ergo, worse general health may contribute to higher risk of heart disease.
12. There does not seem to be a big correlation between eating fruits and vegetables daily and heart disease in this dataset.
13. Neither heavy alcohol consumption or smoking seem to have a significant correlation with heart disease in the current dataset.
14. General Health and Physical Health seem to correlated, suggesting that good physical health may contribute to a good general health. Furthermore, good general health seems to decrease the risk of heart disease. It can be inferred from the data that good physical health, which subsequently leads to good general health, is also quite important in reduciing the risk CVD or MI.

For more visualizations, please refer to the jupyter notebook titled "Exploratory_Data_Analysis_brfss2019.ipynb"

Correlation Matrix for Multivariate Analysis:
![image](https://github.com/hasham-zahid/CIND820-Capstone-Heart-Disease-Prediction/assets/148837970/255557b3-9b0d-4e4a-bf07-da6de2ad8092)


### Handling Imbalanced Data and Feature Selection
The target variable, ‘HeartDisease’, was imbalanced with a 9:1 ratio as illustrated by Figure 1. To solve this problem, Synthetic Minority Oversampling Technique (SMOTE) and RandomUndersampling were used to balance the classes to an acceptable ratio. This was performed on the training data only, and the test set data was left imbalanced to mimic real world scenarios. After testing and consideration, only RandomUndersampling was used to under sample the majority class, instead of SMOTE to oversample, or SMOTE and RandomUndersampling together. After RandomUndersampling the target variable had a 2:3 split which was adequate. This left the training dataset with 49,756 samples and the test set with 22705 samples. 

In terms of feature selection, the following features were removed from the final models due to either being redundant because they are highly correlated with another feature, or because they did not have a high correlation with the target variable. The features removed were education, physical health, fruits, vegetables, mental health, heavy alcohol consumption, smoking, BMI, and physical activity. The final data had 8 features (not including the target variable), which consisted of age, sex, high blood pressure, high cholesterol, stroke, diabetes, income, and general health. 

![image](https://github.com/hasham-zahid/CIND820-Capstone-Heart-Disease-Prediction/assets/148837970/ee9f1e5b-8bb4-46dc-897f-1c13e0304e40) ![image](https://github.com/hasham-zahid/CIND820-Capstone-Heart-Disease-Prediction/assets/148837970/8a4ad995-0647-4861-9538-420ecf3ea14f)


### Results for Predictive Models
| Model | Accuracy | Precision | Recall | F1-Score | Fit Time |
| ----- | -------- | --------- | ------ | -------- | -------- |
| Logistic Regression | 79.2% | 27.9% | 67.3% | 0.394 | 0.14s |
| K-Nearest Neighbors | 78.8% | 26.9 | 64.7% | 0.380 | 0.08s |
| Support Vector Classifier | 78.0% | 27.0% | 69.9% | 0.390 | 40.5s |
| Random Forests | 78.4% | 27.5% | 70.2% | 0.395 | 7.29s |
| XGBoost | 77.9% | 27.1% | 71.2% | 0.393 | 0.11s |

Almost all of the models were very similar in performance metrics, excluding fit times which differed between the various algorithms. The highest accuracy was logisitic regression, with the lowest being XGBoost. Both logisitic regression and XGBoost however had almost identical f1-scores, with logistic regression being slightly better. However, the recall for logistic regression was lower than XGBoost, and since we are dealing with healthcare data where the recall is an important metric, the XGBoost is preferred compared to logistic regression. The fit-times were also different, with XGBoost performing quicker than logistic regression.

In terms of fit time, SVM was the worst performing model with extremely long fit times. This is most likely due to SVM being computationaly complex and the dataset being large, even after undersampling. The quickest model was K-Nearest neighbors, but it also had the lowest f1- score of all the models, and the only f1-score less than 0.39. Random forest classifier was the second longest fit time, but no where near as long as SVM. It also happened to have the best f1-score out of all the models, and average accuracy at 78.41%.

Overall, taking into account the accuracy, the f1-score, the trade off between precision/recall (recall is slightly more important for this specific dataset), and the fit times. The preferred model would be XGBoost. It was the second quickest model to fit at 0.11s, and had a high f1 score at 0.393. The recall was also the highest of all the models at 0.71. The accuracy, despite being the lowest was still good at 77.9%. However, if model fit times are not a problem and the infrastructure to run complex algorithms is avaiable, than the preferred model would have to be random forest classifier, with high recall, f1-score, and accuracy. 

### Results for Feature Importance
In terms of feature importance, both random forests and XGBoost were quite similar, with the top four and bottom four features being the same across both models. High blood pressure, general health, age, and high cholesterol seem to be the most important factors in classification of heart disease. Diabetes, Stroke and Sex also play a role to some degree but not as much as the former features. Income seems to have least affect on determining and classifying heart disease and this was true for both random forest classifier importance and XGBoost importance. In a clinical setting, with some form of health expert or researcher surveying patients or individuals, the most important features to focus on the in the dataset would be age, followed closely by high blood pressure and high cholesterol. General health should also have a significant impact in screening, as it affects multiple areas of life such as physical activity and diet. Sex, previous history of stroke and diabetes should also be important factors to consider.

![image](https://github.com/hasham-zahid/CIND820-Capstone-Heart-Disease-Prediction/assets/148837970/adbf7f88-e0af-4b7a-9b5b-607bb6f243fb)
![image](https://github.com/hasham-zahid/CIND820-Capstone-Heart-Disease-Prediction/assets/148837970/8f9b908d-08d5-4a13-bbbd-a77c9d6fa0b6)

### Conclusions and Further Work

In the technical aspect, the preferred model for this specific dataset and problem would have to XGBoost, due to its high recall, acceptable accuracy, and low fit time. However, if the fit time is not a large problem and the resources are available, then random forest classifier would be preferred as it does perform slightly better than XGBoost overall, suffering only from being computationally expensive. In the clinical aspect of this study, the most important features and concerns that healthcare experts should be looking out for in patients regarding heart disease are: age of the patient (the older the more at risk), whether they have high blood pressure or high cholesterol, and whether their general health is good or not. Sex and previous history of stroke and diabetes may also be important factors to consider.

Overall, the model seems to be good at classifying heart disease but not very good at truly predicting it. In this case of this project, recall was more important that precision due to the sensitive target variable, but a higher precision would still be quite beneficial. This may change with more data, a stronger approach and more powerful predictive techniques. 

Looking forward to the future, this research could further be developed by using more resources to perform a better parameter search. Additionally, deep learning techniques can be employed to discover any other possible solutions to the problem. The study may also benefit from more raw data being utilized for the training and testing. Finally, some other sampling techniques such as AdaSyn may also be used to see if the algorithms perform better.
