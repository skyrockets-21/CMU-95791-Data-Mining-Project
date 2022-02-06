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

### Introduction
Recidivism, defined as an arrest for a new felony or misdemeanor crime within three
years of the supervision start date, is an important measurement of supervision activities during
the entire time people were under supervision or until the date of recidivism for those arrested.

We are interested in discovering patterns behind recidivism and therefore predicting
recidivism using data mining techniques and governmental datasets.

Ideally, with well-understood relationships between recidivism and predictors, we can
hopefully help reduce violent crime, and protect police and other public safety personnel by
reducing recidivism.

### Jupyter Notebook 1:
https://github.com/skyrockets-21/Predicting-Recidivism/blob/main/part1_intro%2Bdata_cleaning.ipynb \
Data Cleaning and Visualizations

### Jupyter Notebook 2: 
https://github.com/skyrockets-21/Predicting-Recidivism/blob/main/part2_question1.ipynb \
Given an individual's criminal record, is he/she likely to recidivate* and what are the main features associated with recidivism?

**Models Used** \
This question can be answered with classification models and feature importance. Here we will explore six classification models as follows:

1. Logistic Regression
2. K-Nearest Neighbors
3. Naive Bayes Classifier
4. Random Forest
5. Boosting (Gradient/ Adaboost)

\*recidivate within 3 years of parole supervision start date

### Jupyter Notebook 3:
https://github.com/skyrockets-21/Predicting-Recidivism/blob/main/part3_question2.ipynb \
If an individual is classified as a potential recidivist, in which year* is he/she likely to recidivate and what features are associated with the difference in arrest years?


Question 2 is a follow-up for Question 1：if an individual is classified as recidivist by the best model from Q1, we would like to predict in which year* the recidivism arrest is likely to occur, and what features are associated with the difference in arrest years.

**Models Used** \
This question can be answered with multi-class classification models and feature importance. Here we will explore four classification models as follows:

1. K-Nearest Neighbors
2. Naive Bayes Classifier
3. Random Forest
4. Gradient Boosting

\*Year 1 if the recidivism arrest occurred in year 

### Jupyter Notebook 4: 
https://github.com/skyrockets-21/Predicting-Recidivism/blob/main/part4_question3%2Bsummary.ipynb \
What are the characteristics of subgroups of recidivists?

For this task, in order to discover the latent structure in our dataset, we use models from unsupervised learning.

**Models Used** \
We focus here the 2 clustering approaches, namely:

1. K-means Clustering
2. Hiearchical Clustering (Agglomerative)

### Dataset Source
https://data.ojp.usdoj.gov/stories/s/daxx-hznc

&copy; Thomas Tam
