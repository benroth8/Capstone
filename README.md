# Capstone

## Introduction
I chose to do a project on spam classification, since it's a relevant and important topic that can incorportate several concepts learned in this course. Additionally, there are many existing datasets for this type of problem.

## Data Preprocessing
I used the CompleteSpamAssassin dataset, downloaded from this link at Kaggle - https://www.kaggle.com/datasets/nitishabharathi/email-spam-dataset. To load and process the data before creating models, I first removed an unnecessary index column, then applied stemming and lemmatization to every email in the dataset. I split the resulting dataset into training and test sets. 

## Model Training/Selection
In order to determine the best model, I performed grid search 3 different types of models - Logistic Regression, Naive Bayes, and Decision Trees - and 2 types of vectorizers - Tfidf vectorizer and Count vectorizer. I used GridSearchCV for each of the 6 combinations to identify the best overall model and its best parameters. Also, I passed the scoring='f1' argument to each GridSearchCV object to provide a balance between precision and recall. The best performing model on this dataset was the Count Vectorizer combined with the Multinomial Naive Bayes classifier. The parameters chosen for the Count Vectorizer were no max features and no stop words. This model achieved an F1 score of about 0.927, which was the best among all the trained models. 

## Results
As mentioned, the best model achieved an F1 score of about 0.927. 

<img width="283" alt="Screenshot 2024-02-19 at 11 10 03 AM" src="https://github.com/benroth8/Capstone/assets/37677064/7bcc7466-bb40-4629-83c9-d9c0dd31c347">

The confusion matrix shows a more detailed view of the model's performance. This model does a good job of accurately distinguishing spam emails from non spam emails, which is very useful for people checking their email.
