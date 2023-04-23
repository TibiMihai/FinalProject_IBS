# Model Card

## Model Description

The objective of the model is to predict whether or not a certain type of company has to be considered as
a distressed based on certain financial diagnostic measurements. Note: a certain type of company means
being SMEs which had bank debts at the starting point of the observation period. The final goal is that
the creditor can intervene in time for the recovery of borrowed amounts, if the company is in a potential
situation of distress, being known that the longer the interventions are postponed, the greater the 
negative consequences on its profitability should be, on the one hand, but with some constrains related to the
checks of false positive cases, on the other hand.

**Input:** 

The datasets consist of instances represented by the one-year “picture” of the company’s financial position, 
meaning nine numerical predictor variables that belongs to several financial ratio groups. To be more precise, 
the groups considered as a significant risk factor in relation to the studied phenomenon are referring to 
financial pattern type, the one year activity development, the profitability, the  commercial credit management, 
the liquidity and the indebtness. All companies were not in distress at the beginning of the observation period.
No explicit relationship between individual instances.

**Output:** 

The output label is binary and represent the distress of the company in one year.

**Model Architecture:** 

The analysis was conducted by involving several models respective Random Forest (RF), Support Vector Machine 
SVM)and Logistic Regression (LR) as standard version, but also certain variants of them tuned with Bayesian 
optimization. A total of twelve models were built, out of which the best 4-5 models were selected take in consideration :
f1_score_class_1 (class of interest) > 0.5 and recall_class1 > 0.5 or recall_class1 > 0.7 and f1_score_class_1 near 0.5. 
Finally, the one that best approach the performance objective mentioned above was chosen.

## Performance

Being a classification problem with some constrains like imbalanced data and business constrains 
 was measured as follows:
-	performance measured with Recall, which captures how often the model misses company distress;
-	overall performance measured with f1_score (for maximum trade-off between Precision-Recall values).

The performance developed by each model was evaluated on a test sample (out of sample). The best model was 
selected, respective a Random Forest model, tuned with Bayesian optimization and it was validated out of sample.

As a summary the figures shows as follows:
Test results: recall_class1(class of interest): 0.61, f1_score_class1(class of interest): 0.5
Validation results: recall_class1(class of interest): 0.71, f1_score_class1(class of interest): 0.59

## Limitations

The following factors may degrade the model’s performance: 
-	the one-year “picture” of the company’s financial position it may be blur in relation to the studied phenomenon due to
 the postponement of the registration of some business events in accounting;
-	the one-year “picture” of the company’s financial position not in line with the economic life cycle, in which it is 
 (it can be in an atypical year);
- the one-year “picture” of the company’s financial position it can be influenced by certain exceptional events that occur 
 on the market in which it operates.
 
 The overall performance of the model (both in term of recall on class of interest as well as in F1 score) leave room for 
 improvement.


## Trade-offs

The main problem of this research is to find the best possible ratio between the model's ability to detect cases of distress
and to generate as few false positives as possible (due to constraints related to the spending budget allocated to the verification 
of these cases). All this under the conditions that the training of the models is done on an imbalance dataset (reduced number of 
cases for the value of interest).
