# Spaceship Titanic - Predicting Dimensional Transport from Kaggle-challenge-group-14

The Spaceship Titanic competition hosted on Kaggle tasks participants with predicting whether passengers aboard a futuristic interstellar cruise were transported to an alternate dimension after a spacetime anomaly.
This project builds a robust machine learning pipeline that includes comprehensive EDA, feature engineering, model building, and evaluation using a combination of statistical methods and machine learning techniques.

## Dataset Overview

  
##  Project Overview

###  Goals:
1. Clean and preprocess the raw data.
2. Perform comprehensive Exploratory Data Analysis (EDA).
3. Engineer meaningful features.
4. Prepare data for modeling (splitting, encoding, scaling).
5. Model train and evaluation 
---

##  Data Cleaning

1.Handling Missing Values:

Median imputation for Age based on passenger group

Zero-spending inference to populate CryoSleep

2.Mode or most frequent values for categorical variables

3.Cabin Feature Engineering:

Split the Cabin into Cabin_Deck, Cabin_Number, and Cabin_Side for better interpretability

4.Additional Engineered Features:

Total_Spending: Combined cost of all onboard services

Is_Alone: Indicates if a passenger traveled without family/group

---
##  Exploratory Data Analysis (EDA)

Univariate Analysis
Numerical: Histograms and KDE plots of Age and Spending features to detect skew and outliers.

Categorical: Count plots for features like HomePlanet, Destination, and Cabin_Deck.

Bivariate Analysis
Categorical vs Target: Bar plots showing Transported rate across CryoSleep, HomePlanet, etc.

Numerical vs Target: KDE and boxplots of Age, Total_Spending, etc., by Transported status.


 Modeling & Evaluation
 ------------------------------
 
Models Used:
## Random Forest Classifier
Tree-based ensemble model

Handles mixed types well and robust to overfitting

Feature importance used for interpretability

## CatBoost Classifier
Gradient Boosted Decision Trees optimized for categorical features

Efficient with missing values and encoding

Best performer in validation (F1-score)

## Logistic Regression
Linear model used as a baseline

Fast to train and easy to interpret

Helped evaluate added value of more complex models

## Model Metrics & Plots

Accuracy, Precision, Recall, F1-score

ROC Curves for each classifier

Confusion Matrices to visualize classification errors

Precision-Recall Curves for imbalance analysis

Feature Importance Plots for interpretability









