# Psychometric_Capstone
By:Seraj Khazei

![Header](https://user-images.githubusercontent.com/81191793/145141983-4eb099f5-1e67-485c-ab7d-6620dd33fcad.png)



###  Overview
Capstone project for Flatiron Data Science BootCamp. In this Project I used various classification algorithms in order to accurately identify indications of trait Neuroticism in individuals via their facebook status updates. I start by importing neccassary packages, cleaning/text preprocessing the data and building my baseline model. I want to be able to accurately classify Neurotic individuals in order to help my stakeholder target ads towards the correct facebook users. Some of my recommendations is to focus on correctly identifying Neurotic individuals as freqent as possible to be able to hone in in the objective as much as possible.

### Stakeholder
Headspace marketing team

### Business Problem
Headspace among everyone in the world has noticed there has been a spike in depression and anxiety since the Pandemic has started. Headspace as being a mediation app understands they are capable of reducing the depression or anxiety rate at any scale, so in order to fufill the following task Headspace has created a special promotion for those who already have mental illness or are of risk to mental illness. Although Headspace needs help to reach the individuals who meet the following requirement. This is where I come in to strategize a way to target the ads towards the following individuals and this notebook will be a demonstration for how the objective was tackled.


### Data
The dataset put into use was acquried from a project conducted by a Data scientist in 2018 here is the link to the project [https://github.com/jcl132/personality-prediction-from-text]. The following dataset takes in 500,000 status updates and scores them on the big five personality trait based on the use of language in the update

### Methods

For methods, I dropped non-relevant columns and assigned neurotic or not neurotic to each status update. I tokenized the status to split each status into its respective words so that each word is a feature in the model. I also remove stopwords as they provide little to no sentiment value to the status. Lemmatization is performed to group words with the same meaning together as one word. TF-IDF is applied in order to assign each word in each facebook status as a numeric value based on its importance across all tweets. Finally, SMOTE is applied in order to eliminate the class imbalance observed in the target variable (sentiment). I used pandas to perform data filtering and visualization, nltk to perform text preprocessing, imblearn for oversampling and pipleline  and sklearn for TF-IDF.For modeling, I utilized the sklearn's LogisticRegression, DecisionTree and RandomForestClassifier methods. I tuned my models using GridSearchCV also provided by sklearn.

My final model has an fbeta score of 83%, which means that it correctly identifies the sentiment of statues 83% of the time. I used a training set and validation set to validate my model performance, and used the test set on my final model.


### Conclusion 
The goal of this project was to come up with a method to identify individuals who show indications of Neuroticism in order to send them promotional ads to ulitmatley try to reduce the recent spike of depression and or anxiety. This was done by creating multiple classification models and identified the best one as a logistic regression model with an fbeta score of 83%. This model will allow our stakeholder to identify the neurotic users and target their ads accordingly.

### For More Information
Please review my full analysis in my [Jupyter Notebook](https://github.com/serajkhazei/Psychometric_Capstone/blob/main/Final_Notebook.ipynb) or my [presentation](https://github.com/serajkhazei/Psychometric_Capstone/blob/main/Capstone_presentation.pdf).
### Repository Structure

```
├── data
│   ├── Final_df.csv
│   ├── master_data.csv
│   └── mypersonality_cleaned.csv
├── Images
│   ├── Decision_con_matrix.png
│   ├── Final_con_matrix.png
│   ├── Freqdist.png
│   ├── Header.png
│   ├── baseline_con-matrix.png
│   ├── business_stat.png
│   ├── logitstic_con_matrix.png
│   ├── random_con_matrix.png
│   ├── target_balanced.png
│   └── target_imbalance.png
├── Notebooks
│   ├── Creating master data frame.ipynb
│   └── First Simple model.ipynb
├── Capstone_presentation.pdf
├── Final_Notebook.ipynb
├── Final_Notebook.pdf
├── README.md
└──environment.yml
