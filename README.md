# FinalProject_IBS
# PROJECT TITLE 


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
100 words to explain what your project is about to a general audience. 


The objective of the model is to predict whether or not a certain type of company has to be considered as
a distressed based on certain financial diagnostic measurements. Note: a certain type of company means
being SMEs which had bank debts at the starting point of the observation period. The final goal is that
the creditor can intervene in time for the recovery of borrowed amounts, if the company is in a potential
situation of distress, being known that the longer the interventions are postponed, the greater the 
negative consequences on its profitability should be,on the one hand, but with some constrains related to 
the checks of false positive cases. on the other hand.

## DATA
A summary of the data you’re using, remembering to include where you got it and any relevant citations. 

The datasets consist of around 1500 instances represented by the one-year “picture” of the company’s financial 
position, meaning nine numerical predictor variables that belongs to several financial ratio groups as well as 
the binary target variabile represented by distress. 
The numerical predictor variables are referring to financial pattern type, the one year activity development, 
the profitability, the  commercial credit management, the liquidity and the indebtness. All companies were not 
in distress at the beginning of the observation period. 

This dataset was created by T. Mihai as a support for solving the task of creating and submitting a portfolio 
project as part of the professional certification program in the field of machine learning and artificial 
intelligence organized by Imperial College Business School.


## MODEL 
A summary of the model you’re using and why you chose it. 

The analysis was conducted by involving several models respective Random Forest (RF), Support Vector Machine 
SVM)and Logistic Regression (LR) as standard version, but also certain variants of them tuned with Bayesian 
optimization. A total of twelve models were built and it was choosed the one that best approach the final goal
mentioned above.



## HYPERPARAMETER OPTIMSATION
Description of which hyperparameters you have and how you chose to optimise them. 

The following hyperparameters were used:

For SVC : C (regularization parameter), kernel (kernel type used by the algorithm) and gamma (Kernel coefficient 
for ‘rbf’, ‘poly’ and ‘sigmoid’).

Note:
	C = adds a penalty for each misclassified data point. If c is small, the penalty for misclassified 
	points is low so a decision boundary with a large margin is chosen at the expense of a greater number of 
	misclassifications;
	Kernel = is a similarity measure, it means the degree of closenes;
	Gamma = controls the distance of influence of a single training point. As the gamma decreases, the regions 
	separating different classes get more generalized.

For logistic regresion: C (inverse of regularization strenght) and solver

Note:
	C = see SVC note;
	solver = algorithm to use in the optimization problem.

For Random Forest: n_estimators (number of tree in a forest), max_depth (max depth of a tree), max_features (number 
of feature to consider for the best split), min_sample_split (minimum number of samples required to split an internal 
node), min_samples leaf(minimum number of samples required to be at a leaf node), criterion (measurement of the quality 
of a split)

Note:
	n_estimators = as increases lead to a more robust aggregate model with less variance;
	
	max_depth = the possible number of feature/value combinations that are taken into account. The deeper the tree, 
	the more splits it has. In an individual tree this causes overfitting, however in Random Forest, it shouldn't be such 
	a problem due to the way the ensemble is built;
	
	min_sample_split= a small value will reduce the variance of the ensemble, at the cost of a higher individual tree bias
	
	min_samples leaf = similar in interpretation to min_sample_split
	
	criterion = not a real rule of thumb to know which one to pick, worth trying both

The hyperparameters optimization was conducted with Bayesian optimization with the default option (Gaussian Process)

## RESULTS
A summary of your results and what you can learn from your model 

The performance developed by each model was evaluated on a test sample (out of sample). The best model was 
selected, respective a Random Forest model, tuned with Bayesian optimization and it was re-validated on a 
validation sample (out of sample).

The summary graph is presented as follows:

![Screenshot](image.png)




## (OPTIONAL: CONTACT DETAILS)
If you are planning on making your github repo public you may wish to include some contact information such as a link to your twitter or an email address. 
