## Predicting Recidivism

---

See my projects in detail:
[This Project's Repo](https://github.com/skyrockets-21/Predicting-Recidivism/) \
[Go to my LinkedIn Page](https://www.linkedin.com/in/thomasyctam/) 

---
![image](https://user-images.githubusercontent.com/22537687/152667377-b2c071fb-1f93-477b-bb03-bcc426a277a1.png)

---

### Team Members:
Jamie Lim, Tina Fung, Thomas Tam 

### Introduction
Recidivism, defined as an arrest for a new felony or misdemeanor crime within three
years of the supervision start date, is an important measurement of supervision activities during
the entire time people were under supervision or until the date of recidivism for those arrested.

We are interested in discovering patterns behind recidivism and therefore predicting
recidivism using data mining techniques and governmental datasets. Ideally, with well-understood relationships between recidivism and predictors, we can
hopefully help reduce violent crime, and protect police and other public safety personnel by
reducing recidivism.

### Dataset
Source: https://data.ojp.usdoj.gov/stories/s/daxx-hznc
This dataset contains 25,835 individuals from the State of Georgia released from Georgia prisons on discretionary parole to the custody of the Georgia Department of Community Supervision (GDCS) for the purpose of post-incarceration supervision between January 1, 2013 and December 31, 2015.

● Number of Possible Target Variables (Y): 4 , all categorical variables Recidivism is measured as an arrest for a new felony or misdemeanor crime within three years of the supervision start date. 

- Recidivism Within 3 years: Binary (0 = No, 1 = Yes) 
- Recidivism_Arrest_Year1: Binary (0 = No, 1 = Yes) 
- Recidivism_Arrest_Year2: Binary (0 = No, 1 = Yes) 
- Recidivism_Arrest_Year3: Binary (0 = No, 1 = Yes)

● Number of Features (Xs): 48

● Number of numerical features: 8 (no. 7 and no. 42-48 in the codebook)

● Number of categorical features: 40

● There are 6 subgroups of features:

Supervision Case Information
Prison Case Information
Prior Georgia Criminal History
Prior Georgia Community Supervision History
Georgia Board of Pardons and Paroles Conditions of Supervision
Supervision Activities|
### Task 0. Understanding the Criminal Justice Systems and Definitions in Georgia
Our team has spent considerable time to firstly understand the criminal justice system while we are looking at the data. Meaningful analysis can only be done with a clear understanding of what and how the data looks like, before we can ask why.

### Task 1. Data Cleaning and Visualizations 
Jupyter Notebook 1 [(Link)](https://github.com/skyrockets-21/Predicting-Recidivism/blob/main/part1_intro%2Bdata_cleaning.ipynb) \\
The goal of this task is to understand the dataset and preprocess for downstream analysis

Preprocessing tasks, including but not limited to:
1. Check null values in the dataset
2. Impute data based on prior knowledge and domain knowledge
3. Create dummy variables for categorical variables
4. Determine which features can be dropped
5. Check for imbalance in the labels

Visualization tasks:

Apply plotting techniques, such as facetgrid, box plot, and correlation plot, to discover interesting relationships 
Below are some examples showing interesting patterns:
<div>
<img src="https://user-images.githubusercontent.com/22537687/162011184-c63a1a6c-fa7a-4bcb-8e68-028ef1e935c7.png" width="500"/>
</div>
![image](https://user-images.githubusercontent.com/22537687/162010681-1b93b24c-e7a4-4508-ab25-964bc940df27.png)

### Task 2.1 Predicting Recidivism (Recidivsed / Not Recidivsed)
Jupyter Notebook 2 [(Link)](https://github.com/skyrockets-21/Predicting-Recidivism/blob/main/part2_question1.ipynb) \\
**Question 1: Given an individual's criminal record, is he/she likely to recidivate* and what are the main features associated with recidivism?**

According to our best model (Gradient Boosting), we discoved employment-related features are the most important features associated with recidivism:
![image](https://user-images.githubusercontent.com/22537687/152690636-10315cd1-b12f-4d96-9689-e6ffe48e5d22.png)

**Models Used** \
This question was answered with classification models and feature importance. Here we explored six classification models as follows:

1. Logistic Regression
2. K-Nearest Neighbors
3. Naive Bayes Classifier
4. Random Forest
5. Boosting (Gradient/ Adaboost)

\*recidivate within 3 years of parole supervision start date

### Task 2.2 Predicting Recidivism (Year 1/2/3)
Jupyter Notebook 3 [(Link)](https://github.com/skyrockets-21/Predicting-Recidivism/blob/main/part3_question2.ipynb) 
**Question 2: If an individual is classified as a potential recidivist, in which year* is he/she likely to recidivate and what features are associated with the difference in arrest years?**


Question 2 is a follow-up for Question 1：if an individual is classified as recidivist by the best model from Q1, we would like to predict in which year* the recidivism arrest is likely to occur, and what features are associated with the difference in arrest years.

**Models Used** \
This question was answered with multi-class classification models and feature importance. Here we explored four classification models as follows:

1. K-Nearest Neighbors
2. Naive Bayes Classifier
3. Random Forest
4. Gradient Boosting

\*For example, `Year 1` if the recidivism arrest occurred in a year 

### Task 3 Clustering and Feature 
Jupyter Notebook 4 [(Link)](https://github.com/skyrockets-21/Predicting-Recidivism/blob/main/part4_question3%2Bsummary.ipynb) 
**Question 3: What are the characteristics of subgroups of recidivists?**

For this task, in order to discover the latent structure in our dataset, we used models from unsupervised learning.

**Models Used** \
We focus here the 2 clustering approaches, namely:

1. K-means Clustering
2. Hiearchical Clustering (Agglomerative)


&copy; Thomas Tam
