------------*------------------*----------------------------*-------------------------------*----------------------------------*--------------------------

Key Points:=

1) Loading the data using .csv file and SQLite Database

2) Data Cleaning: Deduplication

3) Performed the Data Preprocessing on the Review Text. 

    a)Begin by removing the html tags
    
    b) Remove any punctuations or limited set of special characters like , or . or # etc.
    
    c)Check if the word is made up of english letters and is not alpha-numeric
    
    d )Check to see if the length of the word is greater than 2 (as it was researched that there is no adjective in 2-letters)
    
    e) Convert the word to lowercase
    
    f)Remove Stopwords
    
    g)Finally Snowball Stemming the word (it was obsereved to be better than Porter Stemming)
  
  4) Analysed Bag of Words, TF-IDF, Word2Vec techniques and Converted review text into vectors using Avg-Word2Vec, TF-IDF-Word2Vec, TF-IDF weighted Word2Vec techniques.
  
  5) Applied TSNE on Text Bag of Words vectors, Text TF-IDF vectors, Text Average Word2Vec vectors, Text TF-IDF weighted Word2Vec vectors




-----------------------------*-------------------*-------------------------*---------------------------

Data Source: https://www.kaggle.com/snap/amazon-fine-food-reviews
EDA: https://nycdatascience.com/blog/student-works/amazon-fine-foods-visualization/
The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon.
Number of reviews: 568,454
Number of users: 256,059
Number of products: 74,258
Timespan: Oct 1999 - Oct 2012
Number of Attributes/Columns in data: 10

Attribute Information:
a)Id

b)ProductId - unique identifier for the product

c)UserId - unqiue identifier for the user

d)ProfileName

e)HelpfulnessNumerator - number of users who found the review helpful

f)HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not

g)Score - rating between 1 and 5

h)Time - timestamp for the review

i)Summary - brief summary of the review

j)Text - text of the review

Objective:
Given a review, determine whether the review is positive (Rating of 4 or 5) or negative (rating of 1 or 2).



    
