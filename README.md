# Spaceship Titanic - Predicting Dimensional Transport from Kaggle-challenge-group-14

The Spaceship Titanic competition on Kaggle challenges participants to predict whether a passenger was transported to an alternate dimension after a spacetime anomaly disrupted the voyage. This project builds an end-to-end machine learning pipeline including data preprocessing, exploratory data analysis (EDA), feature engineering, and model training and evaluation using various classification algorithms.

## Dataset Overview
The dataset includes demographic, travel, and spending data for passengers aboard the Spaceship Titanic.

Key Features:

Categorical: HomePlanet, CryoSleep, Cabin, Destination, VIP

Numerical: Age, RoomService, FoodCourt, ShoppingMall, Spa, VRDeck

Target Variable: Transported (Boolean – whether the passenger was transported)

Train Set: 8693 rows × 14 columns
Test Set: 4277 rows × 13 columns
Missing values exist across most columns and are handled through imputation and inference.

### Project Objectives

Clean and preprocess the dataset.

Perform thorough exploratory data analysis (EDA).

Engineer new features for improved signal.

Train and tune multiple classification models.

Evaluate model performance and select the best performing model.

Generate predictions for the test set.

##  Data Cleaning

## Data Cleaning & Feature Engineering
 # Missing Value Handling
Numerical Imputation:
Age imputed using group-wise medians.
Spending columns (RoomService, FoodCourt, etc.) filled with 0 if CryoSleep is True.

# Categorical Imputation:
Most frequent value used for columns like HomePlanet, VIP, and Destination.

# Cabin Feature Engineering
Cabin split into:

Cabin_Deck (e.g., A, B, C…)

Cabin_Number (numeric ID)

Cabin_Side (Port or Starboard)

# New Features
Total_Spending: Sum of all spending features

Is_Alone: Indicates if a passenger traveled alone (based on group ID)

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









