### This repository contains solution code and explanation for the competition Machine Learning Challenge #2 - Funding successful projects https://www.hackerearth.com/problem/machine-learning/funding-successful-projects/

#### Problem Statement
Kickstarter is a community of more than 10 million people comprising of creative, tech enthusiasts who help in bringing creative project to life. Till now, more than $3 billion dollars have been contributed by the members in fuelling creative projects. The projects can be literally anything – a device, a game, an app, a film etc.

Kickstarter works on all or nothing basis i.e if a project doesn’t meet it goal, the project owner gets nothing. For example: if a projects’s goal is $500. Even if it gets funded till $499, the project won’t be a success.

Recently, kickstarter released its public data repository to allow researchers and enthusiasts like us to help them solve a problem. Will a project get fully funded ?

In this challenge, the goal is to predict whether a project will get successfully funded or not.

It is a binary classification problem and the metric that the models for this problem is going to be evaluated is accuracy score.

#### Dependencies
1. Python 3+
2. Pandas
3. Numpy
4. Sklearn
5. Matplotlib
6. Seaborn
7. Xgboost
8. time

#### Solution
1. Feature creation and feature engineering was used first of all  
2. 3 experiments were conducted:-  
a) Experiment 1 - Undersampling the train dataset based on time  
b) Experiment 2 - Undersampling the train dataset to get the ratio of majority to minority class in the target variable of train dataset as 0.5  
c) Experiment 3 - Predicting a continuous variable from the features available and then predicting the target class using the continuous variable  

Experiment 2 proved to be the best.

3. Stacking was applied on the undersampled train dataset derived from experiement 2. Stacking consisted of 3 xgboost and 1 logistic regression model.  
4. A simple ensemble model of xgboost, logistic regression and the stacking model was done to produce the submission file.  

#### Final result
<i><b>Our final model with a few tweaks related to the threshold for classifiaction got me a final rank of 25 in the leaderboard.</b></i>

#### Scope for further improvement
1. Better feature selection
2. Better feature engineering
