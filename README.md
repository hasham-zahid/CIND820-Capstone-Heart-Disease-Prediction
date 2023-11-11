# CIND820-Capstone-Heart-Disease-Prediction

#### Tentative Stages of the Project
1. Project proposal: This phase of the project revolves around finding a public and open dataset and seeing if it might be a valid and viable option to meet the projects requirements.
2. Cleaning the dataset: This phase involves cleaning the dataset so that it may be used. This includes handling all outliers, missing values, and standardizing the variables so that the data may be used for analysis and model creation.
3. Initial Analysis and Literature Review: After the dataset has been cleaned and is ready to be used, initial analysis will be performed to see the distribution of features, the correlation between features and size and shape of the dataset. A comprehensive literature review should also be carried out to see how past researchers have employed techinques and answered research questions related to similar or same data. This will be a good guideline in model selection and will also allow us to understand why our project is important as a contribution.
4. Exploratory Data Analysis: After the data has been cleaned, initial analysis has been performed and past research has been considered, exploratory data analysis may proceed. This outlines the general trends in the data, as well as correlation between the target variable and correlation between other variables. This is more in depth than the initial analysis and gives us an insight into how our dataset functions and what inferrances we can make from it. This will also help us with feature selection for our models.
5. Feature selection and handling imbalanced data (if any): Before we can begin with our model, feature selection must be performed to see which features we will include in our final models or not. After the features have been selected (either removed or kept in the dataset), we can begin handling our imbalanced data (if there is any). This can involve multiple things, such as splitting the dataset into a train/test split and then performing either oversampling or undersampling (or both) on the TRAIN set only, so that our test set can be used as a reliable real world example of our models.
6. Creating the models and feature importance: The literature review helped us choose which models would be most approraite for our dataset, and feature selection and imbalanced data will help us have a model that can be as accurate as possible to the best our abilities. Each model will be cross validated and performance metrics will be recorded, as well as the fit times. Features that were most important in the models will also be recoreded.
7. Model Comparision: Comparing our models to see which was the overall most effective, taking into account both model performance and model fit time.
8. Final Report: A final report compiling, revising and aggregating all the above stages into one file.
9. Final Presentation: Condensing the most vital aspects of the final report into a presentation that can be interpreted and understood by stakeholders.


 #### File Legend
 1. heart_disease_brfss2019.csv --> The cleaned dataset
 2. brfss2019_cleaning_data.ipynb --> the notebook used to clean the dataset
 3. brfss2019_heart_disease_initial analysis.ipynb --> the initial analysis of the dataset. This notebook also includes attribute information and project goals
 4. brfss_EDA_heart_disease.ipynb --> exploratory data analysis notebook
 5. brfss_ML_models_heart_disease.ipynb --> notebook comprising of feature selection, handling imbalanced target variable, creating machine learning models, feature importance, and finally model comparisions. This file gives insight into how well the models performed and important features in classification.
