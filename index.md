## Predicting Recidivism

---

See my projects in detail:
[This Project's Repo](https://github.com/skyrockets-21/Predicting-Recidivism/) \
[Back to my GitHub Homepage](https://skyrockets-21.github.io/) \
[Go to my LinkedIn Page](https://www.linkedin.com/in/thomasyctam/) 

---
![image](https://user-images.githubusercontent.com/22537687/152667377-b2c071fb-1f93-477b-bb03-bcc426a277a1.png)

---

### Team Members:
Jamie Lim, Tina Fung, Thomas Tam 

---

### Introduction
Recidivism, defined as an arrest for a new felony or misdemeanor crime within three
years of the supervision start date, is an important measurement of supervision activities during
the entire time people were under supervision or until the date of recidivism for those arrested.

We are interested in discovering patterns behind recidivism and therefore predicting
recidivism using data mining techniques and governmental datasets.

Ideally, with well-understood relationships between recidivism and predictors, we can
hopefully help reduce violent crime, and protect police and other public safety personnel by
reducing recidivism.

### Question 1: 
Given an individual's criminal record, is he/she likely to recidivate* and what are the main features associated with recidivism?

For this task, we pick Recidivism_Within_3Years as our target variable and use the rest variables excluding Recidivism_Arrest_Year1, Recidivism_Arrest_Year2, and Recidivism_Arrest_Year3 as features.

The question can be answered with classification models and feature importance. Here we will explore six classification models as follows:

1. Logistic Regression
2. K-Nearest Neighbors
3. Naive Bayes Classifier
4. Random Forest
5. Boosting (Gradient/ Adaboost)

\*recidivate within 3 years of parole supervision start date

### Question 2:
If an individual is classified as a potential recidivist, in which year* is he/she likely to recidivate and what features are associated with the difference in arrest years?

For this task, we are only look at a subset of the cleaned dataset: people who recidivated within 3 years (`Recidivism_Within_3years` == 1). We construct a new Year variable as our target by encoding `Recidivism_Arrest_Year1`,`Recidivism_Arrest_Year2`,`Recidivism_Arrest_Year3` to a categorical variable with 3 classes (1,2,3). We use the rest variables excluding `Recidivism_Within_3years`,`Recidivism_Arrest_Year1`,`Recidivism_Arrest_Year2`, and `Recidivism_Arrest_Year3` as features.

Question 2 is a follow-up for Question 1：if an individual is classified as recidivist by the best model from Q1, we would like to predict in which year* the recidivism arrest is likely to occur, and what features are associated with the difference in arrest years.

### Question 3: 
What are the characteristics of subgroups of recidivists?

For this task, in order to discover the latent structure in our dataset, we use models from unsupervised learning.

Models: We focus here the 2 well-known clustering approaches, namely:

1. K-means Clustering
2. Hiearchical Clustering (Agglomerative)

Data Preparation:

The 4 target variables `Recidivism_Within_3years`,`Recidivism_Arrest_Year1`, `Recidivism_Arrest_Year2`, `Recidivism_Arrest_Year3` are dopped in this section.
Only the top 7 features identified in Question 1 are used here, namely `Percent_Days_Employed`,`Jobs_Per_Year`,`Prior_Arrest_Episodes_PPViolationCharges`,`Age_at_Release`, `Gang_Affiliated`,`Supervision_Risk_Score_First`,`Prior_Arrest_Episodes_Felony`, and unlike prediction task, we do not have to split the dataset into training and testing sets

Technically, we are using KMeans and AgglomerativeClustering from sklearn

### Dataset Source
https://data.ojp.usdoj.gov/stories/s/daxx-hznc

&copy; Thomas Tam
