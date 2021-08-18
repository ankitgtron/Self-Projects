----------------**-------------------------------**---------------------**-----------------------------

Key Points:=
1. Used Pandas to Load the dataset
2. Removed all the duplicate questions.
3. Analysed the tags and major findings are - 

    a)There are total 153 tags which are used more than 10000 times.
    
    b)14 tags are used more than 100000 times.
    
    c)Most frequent tag (i.e. c#) is used 331505 times.
    
    d)Since some tags occur much more frequenctly than others, Micro-averaged F1-score is the appropriate metric for this probelm.
4. Preprocessing

    a)Sample 1M data points
    
    b)Separate out code-snippets from Body
    
    c)Remove Spcial characters from Question title and description (not in code)
    
    d)Remove stop words (Except 'C')
    
    e)Remove HTML Tags
    
    f)Convert all the characters into small letters
    
    g)Use SnowballStemmer to stem the words
    
 5. Apply Logistic Regression with OneVsRest Classifier

      a)accuracy : 0.081965
      
      b)macro f1 score : 0.0963020140154
      
      c)micro f1 scoore : 0.374270748817
      
      d)hamming loss : 0.00041225090909090907


------------------**----------------------------**------------------------------------------------------------------

Description -
Stack Overflow is the largest, most trusted online community for developers to learn, share their programming knowledge, and build their careers.
Stack Overflow is something which every programmer use one way or another. Each month, over 50 million developers come to Stack Overflow to learn, share their knowledge, and build their careers. It features questions and answers on a wide range of topics in computer programming. The website serves as a platform for users to ask and answer questions, and, through membership and active participation, to vote questions and answers up or down and edit questions and answers in a fashion similar to a wiki or Digg. As of April 2014 Stack Overflow has over 4,000,000 registered users, and it exceeded 10,000,000 questions in late August 2015. Based on the type of tags assigned to questions, the top eight most discussed topics on the site are: Java, JavaScript, C#, PHP, Android, jQuery, Python and HTML.

Problem Statement - 
The task is to predict the tags (a.k.a. keywords, topics, summaries), given only the question text and its title. The dataset contains content from disparate stack exchange sites, containing a mix of both technical and non-technical questions.
Source: https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/
Data Source : https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data

Real World / Business Objectives and Constraints 
1. Predict as many tags as possible with high precision and recall.
2. Incorrect tags could impact customer experience on StackOverflow.
3. No strict latency constraints.
Refer: https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data

All of the data is in 2 files: Train and Test.
Train.csv contains 4 columns: Id,Title,Body,Tags.
Test.csv contains the same columns but without the Tags, which you are to predict.
Size of Train.csv - 6.75GB
Size of Test.csv - 2GB
Number of rows in Train.csv = 6034195
The questions are randomized and contains a mix of verbose text sites as well as sites related to math and programming. The number of questions from each site may vary, and no filtering has been performed on the questions (such as closed questions).

Data Field Explaination
Dataset contains 6,034,195 rows. The columns in the table are:
Id - Unique identifier for each question
Title - The question's title
Body - The body of the question
Tags - The tags associated with the question in a space-seperated format (all lowercase, should not contain tabs '\t' or ampersands '&')

Performance metric
Micro-Averaged F1-Score (Mean F Score) : The F1 score can be interpreted as a weighted average of the precision and recall, where an F1 score reaches its best value at 1 and worst score at 0. The relative contribution of precision and recall to the F1 score are equal. The formula for the F1 score is:
F1 = 2 * (precision * recall) / (precision + recall)
In the multi-class and multi-label case, this is the weighted average of the F1 score of each class.
'Micro f1 score':
Calculate metrics globally by counting the total true positives, false negatives and false positives. This is a better metric when we have class imbalance.
'Macro f1 score':
Calculate metrics for each label, and find their unweighted mean. This does not take label imbalance into account.
https://www.kaggle.com/wiki/MeanFScore
http://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html

