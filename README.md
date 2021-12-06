# Flatiron_Capstone
By:Seraj Khazei


![image](https://user-images.githubusercontent.com/81191793/144152128-ac1c4792-819d-4c53-a1a2-1fce024a3264.png)



###  Overview
Project four for Flatiron Data Science BootCamp. In this Project we used various classification algorithms In this project in order to identify neurotic individuals based on their neurticism score and the language used in the status update. The dataset includes more than 500,000 status updates. This dataset is well-suited for the business problem, as the goal is to identify neurotic individuals in order to send them ads for headspace.

### Stakeholder
Headspace marketing team

### Business Problem
Headspace among everyone in the world has noticed there has been a spike in depression and anxiety since the Pandemic has started. Headspace as being a mediation app understands they are capable of reducing the depression or anxiety rate at any scale, so in order to fufill the following task Headspace has created a special promotion for those who are already have mental illness or are of risk to mental illness. Although Headspace needs help to reach the individuals who meet the following requirement. This is where I come in to strategize a way to target the ads towards the following individuals and this notebook will be a demonstration for how the objective was tackled.


### Data
The dataset was acquired from https://aaai.org/Library/Workshops/ws13-01.php
which takes in various facebook statuses and scores the status on the big 5 peronality trait 

### Methods

For methods, I dropped non-relevant columns and assigned neurotic or not neurotic to each status update. Then, I used "re" libary to get rid of unimportant characters in the status update. After that, I tokenize the status to split each status into its respective words so that each word is a feature in the model. We also remove stopwords as they provide little to no sentiment value to the status. Lemmatization is performed to group words with the same meaning together as one word. TF-IDF is applied in order to assign each word in each tweet a numeric value based on its importance across all tweets. Finally, SMOTE is applied in order to eliminate the class imbalance observed in the target variable (sentiment). We used pandas to perform data filtering and visualization, nltk to perform text preprocessing, imblearn for oversampling and sklearn for TF-IDF.For modeling, I utilized the sklearn's LogisticRegression, DecisionTree and RandomForestClassifier methods. I tuned our models using GridSearchCV also provided by sklearn.

Our final model has an f1 score of 84%, which means that it correctly identifies the sentiment of statues 84% of the time. I used a validation set and the test set f1 scores in order to validate our model performance.


### Conclusion 
The goal of this project was to come up with a method to identify individuals who show indications of Neuroticism in order to send them promotional ads to ulitmatley try to reduce the recent spike of depression and or anxiety. This was done by creating multiple classification models and identified the best one as a logistic regression model with an f1 of 84%. This model will allow our stakeholder to identify the neurotic users and target their ads accordingly.
