# Spaceship Titanic - Predicting Dimensional Transport from Kaggle-challenge-group-14

The Spaceship Titanic competition hosted on Kaggle tasks participants with predicting whether passengers aboard a futuristic interstellar cruise were transported to an alternate dimension after a spacetime anomaly.
This project builds a robust machine learning pipeline that includes comprehensive EDA, feature engineering, model building, and evaluation using a combination of statistical methods and machine learning techniques.

## Dataset Overview

The dataset contains personal and spending data for thousands of passengers. The key features include:

Categorical Features:

HomePlanet, CryoSleep, Cabin, Destination, VIP

Numerical Features:

Age, RoomService, FoodCourt, ShoppingMall, Spa, VRDeck

Target Column:

Transported: Boolean indicating if the passenger was transported to another dimension

Column Descriptions : 
PassengerId - A unique Id for each passenger. Each Id takes the form gggg_pp where gggg indicates a group the passenger is travelling with and pp is their number within the group. People in a group are often family members, but not always.
HomePlanet - The planet the passenger departed from, typically their planet of permanent residence.
CryoSleep - Indicates whether the passenger elected to be put into suspended animation for the duration of the voyage. Passengers in cryosleep are confined to their cabins.
Cabin - The cabin number where the passenger is staying. Takes the form deck/num/side, where side can be either P for Port or S for Starboard.
Destination - The planet the passenger will be debarking to.
Age - The age of the passenger.
VIP - Whether the passenger has paid for special VIP service during the voyage.
RoomService, FoodCourt, ShoppingMall, Spa, VRDeck - Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities.
Name - The first and last names of the passenger.
Transported - Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.

  Observations in Train Data:
* There are total of 14 columns and 8693 rows in train data.
* Train data contains 119378 observation with 2324 missing values.
* All 12 feature columns have missing values in them with CryoSleep having highest missing values (217)
* Transported is the target variable which is only available in the train dataset.

  Observations in Test Data:
* There are total of 13 columns and 4277 rows in test data.
* Train data contains 54484 observation with 1117 missing values.
* All 12 feature columns have missing values in them with FoodCourt having highest missing values (106)

  
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

## 1. Univariate Analysis

Numerical Features

Histograms + KDE for distribution

Boxplots to detect outliers and spread

Categorical Features

Count plots for key columns like HomePlanet, Destination, Cabin_Deck, etc.

### 2. Bivariate Analysis

Target vs Numerical Features

Box and violin plots

KDE overlays comparing Transported classes

Target vs Categorical Features

 Modeling & Evaluation
 ------------------------------
 
Models Used:
 Random Forest Classifier
Tree-based ensemble model

Handles mixed types well and robust to overfitting

Feature importance used for interpretability

 CatBoost Classifier
Gradient Boosted Decision Trees optimized for categorical features

Efficient with missing values and encoding

Best performer in validation (F1-score)

 Logistic Regression
Linear model used as a baseline

Fast to train and easy to interpret

Helped evaluate added value of more complex models







