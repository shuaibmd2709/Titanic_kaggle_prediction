# Titanic_kaggle_prediction

A Machine Learning Classification Project

This project builds and tests different binary classification models to predict whether a passenger survived the tragic sinking of the RMS Titanic.

Using the data provided by the most famous competition hosted by Kaggel, I have performed the following actions:
 * Exploratory Data Analysis
 * Feature Engineering
 * Model defination
 * Prediction
 * Performation Metrics Comparision

Dataset Info()

*Age
*Name
*Sex
*Passenger Class
*Ticket
*Cabin
*Fare
*Family relationships (SibSp, Parch)
*Embarkation port
*Survived

Exploratory Data Analysis:
 - On df.info(), it is understood that, the data consists of both Categorical and Numerical columns.
 - A simple count plot is plotted to have an idea on Survived vs Non-Survived passengers.
 - The ratio of male vs female survival rate is plotted. From the plot, it is understood that most passengers survived were Females.
 - When a camparision is done between the Passenger Class survival count, PClass 1 has the most Survivers.
 - As the Age column has missing data.Before missing values are imputed, the strategy needs to be choosen. The distribution is not skwed and the the value was 0.36. Therefore mean as a strategy to fillup missing values would be a great choice.
 - Fare column is right skwed and log transformer would be later used to reduced the skweness.

Feature Engineering:
 - Columns, Name, Ticket, Embarakation port, Cabin are dropped as they hold no significant knowleadge through which the model would learn.
 - Before Feature Engineering is performed, the dataset is split into train and test in order to aviod any kind of leakage.
 - OneHotEncoding is done on Sex column to convert categorical values to Numercial Values.
 - SimpleImputer with mean as strategy as discussed earlier is applied to Age to handle missing values.
 - Log Transformer is applied on the Fare column to normalise the values. Before transform Skew score: 4.7, After transform Skew score: 0.39.

Model Selection:
 - As the current problem is a binary classification problem, three different models have been selected.
 - Logistic Regression, Random Forest Classifier(Best for Classification) and Gradient Boost Classifier.

Performance Comparision:

 Model| Accuracy_Score
 ----------------------
 LR   | 0.81
 
 RFC  | 0.79
 
 GBC  | 0.80

 
