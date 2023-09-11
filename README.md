# Heart-disease-classification
Predicting heart disease using machine learning
This notebook looks into using various Python-based machine learning and data science libraries in an attempt to build a machine learning model capable of predicting whether or not someone has heart disease based on their medical attributes

More specifically, we'll look at the following topics.
Exploratory data analysis (EDA) - the process of going through a dataset and finding out more about it.
Model training - create model(s) to learn to predict a target variable based on other variables.
Model evaluation - evaluating a models predictions using problem-specific evaluation metrics.
Model comparison - comparing several different models to find the best one.
Model fine-tuning - once we've found a good model, how can we improve it?
Feature importance - since we're predicting the presence of heart disease, are there some things which are more important for prediction?
Cross-validation - if we do build a good model, can we be sure it will work on unseen data?
Reporting what we've found - if we had to present our work, what would we show someone?
To work through these topics, we'll use pandas, Matplotlib and NumPy for data anaylsis, as well as, Scikit-Learn for machine learning and modelling tasks.

Approach:
Understanding Problem
Data
Evaluation
Features
Modelling
Experimentation
1. Understanding Problem
In our case, the problem we will be exploring is binary classification (a sample can only be one of two things).

This is because we're going to be using a number of differnet features (pieces of information) about a person to predict whether they have heart disease or not.

In a statement

Given clinical parameters about a patient, can we predict whether or not they have heart disease?

2. Data
Got data from kaggle. : https://www.kaggle.com/datasets/sumaiyatasmeem/heart-disease-classification-dataset?select=heart+disease+classification+dataset.csv

The original database contains 76 attributes, but here only 14 attributes will be used. Attributes (also called features) are the variables what we'll use to predict our target variable.

Attributes and features are also referred to as independent variables and a target variable can be referred to as a dependent variable.

We use the independent variables to predict our dependent variable.

Or in our case, the independent variables are a patients different medical attributes and the dependent variable is whether or not they have heart disease.

3. Evaluation
If we can reach 95% accuracy at predicting whether or not a patient has heart disease during the proof of concept, we will pursue the project'

4. Features
This is where you will get different information about each of the features in your data

** Data dictionary **

1. age - age in years
2. sex - (1 = male; 0 = female)
3. cp - chest pain type 
    * 0: Typical angina: chest pain related decrease blood supply to the heart 
    * 1: Atypical angina: chest pain not related to heart 
    * 2: Non-anginal pain: typically esophageal spasms (non heart related) 
    * 3: Asymptomatic: chest pain not showing signs of disease 
4. trestbps - resting blood pressure (in mm Hg on admission to the hospital) anything above 130-140 is typically cause for concern
5. chol - serum cholestoral in mg/dl 
    * serum = LDL + HDL + .2 * triglycerides 
    * above 200 is cause for concern 
6. fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) 
    * '>126' mg/dL signals diabetes 
7. restecg - resting electrocardiographic results 
    * 0: Nothing to note 
    * 1: ST-T Wave abnormality 
    * can range from mild symptoms to severe problems 
    * signals non-normal heart beat 
    * 2: Possible or definite left ventricular hypertrophy 
    * Enlarged heart's main pumping chamber
8. thalach - maximum heart rate achieved
9. exang - exercise induced angina (1 = yes; 0 = no) 
10. oldpeak - ST depression induced by exercise relative to rest looks at stress of heart during excercise unhealthy heart will stress more
11. slope - the slope of the peak exercise ST segment 
    * 0: Upsloping: better heart rate with excercise (uncommon) 
    * 1: Flatsloping: minimal change (typical healthy heart) 
    * 2: Downslopins: signs of unhealthy heart 
12. ca - number of major vessels (0-3) colored by flourosopy 
    * colored vessel means the doctor can see the blood passing through 
    * the more blood movement the better (no clots) 
13. thal - thalium stress result 
    * 1,3: normal 
    * 6: fixed defect: used to be defect but ok now\n 
    * 7: reversable defect: no proper blood movement when excercising 
14. target - have disease or not (1=yes, 0=no) (= the predicted attribute) 
**Note: No personal identifiable information (PPI) can be found in the dataset.

It's a good idea to save these to a Python dictionary or in an external file, so we can look at them later without coming back here.

The Tools
pandas for data analysis.
NumPy for numerical operations.
Matplotlib/seaborn for plotting or data visualization.
Scikit-Learn for machine learning modelling and evaluation.
we're going to use Pandas, Matplotlib and Numpy for data analysis and manipulation
