---------------------**-----------------------**-----------------------**--------------------

Key Points :-

1. Split the dataset randomly into three parts train, cross validation and test with 64%,16%, 20% of data respectively

2. Preprocessing of text

3. Prediction using a 'Random' Model

4. completed Univariate analysis.

5. Used different vectorizer Gene Feature One-Hot, Text Feature One-Hot for applying Linear SVM.

6. Used TfIdf Features vectorizer and applied Naive Bayes and Mltinomial Naive Bayes classification algorithm to minimize the multi class log loss.

7. Applied K Nearest Neighbors classification algorithm.

------------------------**----------------------**--------------------------------------------------

Personalized cancer diagnosis

Description
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/
Data: Memorial Sloan Kettering Cancer Center (MSKCC)
Download training_variants.zip and training_text.zip from Kaggle.

Context:
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/discussion/35336#198462

Problem statement :
Classify the given genetic variations/mutations based on evidence from text-based clinical literature.

Real-world/Business objectives and constraints.
No low-latency requirement.
Interpretability is important.
Errors can be very costly.
Probability of a data-point belonging to each class is needed.


Data Overview
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/data
We have two data files: one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that human experts/pathologists use to classify the genetic mutations.
Both these data files are have a common column called ID

Data file's information:
training_variants (ID , Gene, Variations, Class)
training_text (ID, Text)

Performance Metric
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment#evaluation

Metric(s):
Multi class log-loss
Confusion matrix

Machine Learing Objectives and Constraints
Objective: Predict the probability of each data-point belonging to each of the nine classes.

Constraints:
Interpretability, Class probabilities are needed.
Penalize the errors in class probabilites => Metric is Log-loss. 
No Latency constraints.




 

