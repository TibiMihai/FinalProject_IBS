# Datasheet Template

As far as you can, complete the model datasheet. If you have got the data from the internet, you may not have all the information you need, but make sure you include all the information you do have. 

## Motivation

- For what purpose was the dataset created?

The objective of the dataset is to predict based on an analysis of three models (Random Forest (RF), Support Vector Machine (SVM) and Logistic Regression (LR)) whether or not a 
certain type of company has to be considered in a distressed based on certain financial diagnostic measurements included in the dataset. Several constraints were placed in order to select this 
certain type of companies from a larger database. In particular, all companies are SMEs and had bank debts at the starting point of the observation period


- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?

This dataset was created by T. Mihai as a support for solving the task of creating and submitting a portfolio project as part of the professional certification program 
in the field of machine learning and artificial intelligence organized by Imperial College Business School.
 
## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? 

The datasets consist of several financials’ predictor variables and one target variable, Distress Framework. Predictor variables are part of several financial ratio groups, 
respectively: financial pattern, 1 year activity development, profitability, commercial credit management, liquidity and indebtness.

- How many instances of each type are there?

1558 companies were selected. All companies were not in distress at the beginning of the observation period. At the end, about 10% were in distress, the problem falling under the topic 
of imbalanced data. The selection of train, validation and testing samples was done randomly. The population for this is larger and focused only on one market. The proposed dataset 
is only a sample. In the selection, several criteria were followed to ensure some representativeness, such as size, financial pattern and local geographical area. However, the dataset
remains a particular one (related to a certain market, a certain segment of companies, etc.). Each instance consists of nine numerical variables which were chosen to form the basis for forecasting 
the distress within one year. Those variables were chosen because it addresses the main categories of financial aspects considered as a significant risk factor in relation to the studied phenomenon.
The output label is binary and represent the distress of the company in one year.
No explicit relationship between individual instances.
The research objective can be assigned to the imbalanced data for a classification topic (the target class has an uneven distribution of observations) for which the preparation of development 
data requires greater attention than in standard cases. For this study, oversampling, cross validation was used alongside with the standard approach (which had the benchmark role). 
The dataset was divided into train, test and validation. The dataset is entirely self-contained.

 
- Is there any missing data?

Everything is included. No data is missing.

- Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor–patient confidentiality, data that includes the content 
of individuals’ non-public communications)?

The dataset contains info about financial information of companies made public through the annual statements. However, the data were anonymized and transformed to limit the possibility of identification.


## Collection process

- How was the data acquired?

The dataset contains info about financial information of companies made public through the annual statements. However, the data were anonymized and transformed to limit the possibility of identification.

- If the data is a sample of a larger subset, what was the sampling strategy?

The population from which the dataset originates is larger. In the selection of the dataset, several criteria were followed to ensure representativeness, such as size, financial pattern and geographical area.

- Over what time frame was the data collected?

The data have a time horizon of 1 year. All companies were not in distress at the beginning of the observation period. At the end, about 10% were in distress.

## Preprocessing/cleaning/labelling

- Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, 
processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section. 

The data set was pre-processed compared to the initial one, respectively the data were transformed to limit the possibility of identification, were labelled, the outliers were replaced with
the 0.05 and 0.95 percentiles and standardization was applied.


- Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? 
 
The “raw” data were saved in addition to the pre-processed / cleaned / labelled data.
 

## Uses

- What other tasks could the dataset be used for? 

The dataset should be used for the research of the topic for which it was intended.

- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example,
 is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) 
 or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms? 
 
 The dataset contains info about financial information of companies made public through the annual statements. Even if, the data were anonymized and transformed to limit the possibility of identification, 
 there is a risk of harm if they are identified.
 
 
- Are there tasks for which the dataset should not be used? If so, please provide a description.

It should be noticed that the data set is a particular one, intended for the research of the theme of this project.


## Distribution

- How has the dataset already been distributed? 

The data set was not distributed, it was created and proposed only for the purpose of this project. The dataset is part of the project mentioned above and it is submitted on github.


- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)? 

This dataset was created by T. Mihai as a support for solving the task of creating and submitting a portfolio project as part of the professional certification program 
in the field of machine learning and artificial intelligence organized by Imperial College Business School.

## Maintenance

- Who maintains the dataset?

The maintenance of this data set was not foreseen