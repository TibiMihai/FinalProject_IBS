# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

The objective of the model is to predict whether or not a certain type of company has to be considered as
a distressed based on certain financial diagnostic measurements. Note: a certain type of company means
being SMEs which had bank debts at the starting point of the observation period. The final goal is that
the creditor can intervene in time for the recovery of borrowed amounts, if the company is in a potential
situation of distress, being known that the longer the interventions are postponed, the greater the 
negative consequences on its profitability should be, on the one hand, but with some constrains related to the
checks of false positive cases. on the other hand.

**Input:** Describe the inputs of your model 

The datasets consist of instances represented by the one-year “picture” of the company’s financial position, 
meaning nine numerical predictor variables that belongs to several financial ratio groups. To be more precise, 
the groups considered as a significant risk factor in relation to the studied phenomenon are referring to 
financial pattern type, the one year activity development, the profitability, the  commercial credit management, 
the liquidity and the indebtness. All companies were not in distress at the beginning of the observation period.
No explicit relationship between individual instances.

**Output:** Describe the output(s) of your model

The output label is binary and represent the distress of the company in one year.



**Model Architecture:** Describe the model architecture you’ve used

The analysis was conducted by involving several models respective Random Forest (RF), Support Vector Machine 
SVM)and Logistic Regression (LR) as standard version, but also certain variants of them tuned with Bayesian 
optimization. A total of twelve models were built and the one that best approach the performance objective 
explained below was chosen.

## Performance
Give a summary graph or metrics of how the model performs. Remember to include how you are measuring the 
performance and what data you analysed it on. 

Being a classification problem with some constrains like imbalanced data and business constrains 
 was measured as follows:
-	performance measured with Recall, which captures how often the model misses company distress;
-	overall performance measured with f1_score (for maximum trade-off between Precision-Recall values).

The performance developed by each model was evaluated on a test sample (out of sample). The best model was 
selected, respective a Random Forest model, tuned with Bayesian optimization and it was re-validated on a 
validation sample (out of sample).

The summary graph is presented as follows:

![Screenshot](image1.png)


## Limitations

Outline the limitations of your model.

The following factors may degrade the model’s performance: 
-	the limited number of companies in distress, a fact that is limiting the learning performance of the model;
-	the one-year “picture” of the company’s financial position it may be:
1)	blur in relation to the studied phenomenon due to the postponement of the registration of some events
in accounting;
2)	not in line with the economic life cycle, in which it is (it can be in an atypical year)
3)	influenced by certain exceptional events that occur on the market in which it operates

Under these conditions, the model has a relatively good capacity to detect cases of distress, but it fails to 
properly balance the trade-off between precision and recall, registering a relatively low value of the f1 score.


## Trade-offs

Outline any trade-offs of your model, such as any circumstances where the model exhibits performance issues. 

Mainly, the trade-off is related to the need to identify as many cases of distress as possible, on the one hand, 
and the budget limit that the creditor has available to analyse false positive cases. 