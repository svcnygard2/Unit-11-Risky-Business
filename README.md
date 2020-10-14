# Unit-11-Risky-Business
Peer-to-peer lending services such as LendingClub or Prosper allow investors to loan other people money without the use of a bank. However, investors always want to mitigate risk.
- I will build and evaluate several machine-learning models to predict credit risk using free data from LendingClub.
- I will use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the resampling and ensemble learning techniques.
## Libraries Needed:
- numpy
- pandas
- pathlib
- collections
- sklearn.metrics
- sklearn.preprocessing
- sklearn.model_selection
- sklearn.linear_model
- imblearn.over_sampling
- imblearn.metrics
- imblearn.ensemble
## Tips:
- Remember to restart kernel incase of "bugs".
- Give the code time to run - if there is an asterisks(*) by the algorithm, just let it run.
## Resampling Questions:
### 1. Which model had the best balanced accuracy score?
The Naive Random Oversampling model has the highest balanced accuracy score of 0.7201775908400514.  Accuracy is how often the model is correct but a weakness of the  score is that it does not calculate precision well.
### 2. Which model had the best recall score?
Recall is the ratio of correctly predicted positive observations to all predicted observations for that class. For this model, I want to maximize the low_risk recall classification rate so I could maximize the revenue potential.  The model with the highest recall rate for low risk class borrowers was the SMOTE oversampling model at 0.78.
### 3. Which model had the best geometric mean score?
The model with the best geometric mean score is the SMOTEENN - Combination Sampling model at 0.72.  There was an initial tie between two models' geometric mean score, that being the SMOTEENN - Combination Sampling model and the Naive Random Oversampling at 0.72.  How I came upon the SMOTEENN model being the best was by calculating the test and training data scores for both models and finding out which is most stable - which score has the least variance.  The SMOTEENN training score is 0.753545687 and the testing score is 0.75483871 with a variance of 0.001293023.  The Naive Random Oversampling traing score is 0.771274122 and the testing score is 0.773147341 with a variance of 0.001873219.
## Ensemble Questions:
### 1. Which model had the best balanced accuracy score?
The Easy Ensemble Classifier model has the highest balanced accuracy score of 0.7633646373448397. This is the ratio of correctly predicted observations to the total number of observations.  One weakness of the accuracy score is that it does not communicate how precise it is.
### 2. Which model had the best recall score?
High recall relates to a more comprehensive output and a low false negative rate.  TP/(TP+FN).  I want to maximize the low_risk recall classification rate so I could maximize the revenue potential.  The model with the highest recall rate for low risk class borrowers was the Balanced Random Forest Classifier model at 0.86.
### 3. Which model had the best geometric mean score?
The best model for finding the best geometric mean score is the Easy Ensemble Classifier model at 0.76.
### 4. What are the top three features?
The top three features model are total_rec_int with a feature importanc of 0.07708262333848419, total_rec_prncp with a feature importance of 0.0671568345430142, and total_pymnt with a feature importance of 0.065911828691246.
