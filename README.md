# Spaceship Titanic - Predicting Dimensional Transport Kaggle-challenge-group-14

Spaceship Titanic - Predicting Dimensional Transport

The Spaceship Titanic competition hosted on Kaggle tasks participants with predicting whether passengers aboard a futuristic interstellar cruise were transported to an alternate dimension after a spacetime anomaly.
This project builds a robust machine learning pipeline that includes comprehensive EDA, feature engineering, model building, and evaluation using a combination of statistical methods and machine learning techniques.

2.Install requirements:

pip install -r requirements.txt

## Dataset Overview

The dataset contains personal and spending data for thousands of passengers. The key features include:

Categorical Features:

HomePlanet, CryoSleep, Cabin, Destination, VIP

Numerical Features:

Age, RoomService, FoodCourt, ShoppingMall, Spa, VRDeck

Target Column:

Transported: Boolean indicating if the passenger was transported to another dimension

  
##  Project Overview

###  Goals:
1. Clean and preprocess the raw data.
2. Perform comprehensive Exploratory Data Analysis (EDA).
3. Engineer meaningful features.
4. Prepare data for modeling (splitting, encoding, scaling).
---

##  Data Cleaning

Handling Missing Values:

Median imputation for Age based on passenger group

Zero-spending inference to populate CryoSleep

Mode or most frequent values for categorical variables

Cabin Feature Engineering:

Split the Cabin into Cabin_Deck, Cabin_Number, and Cabin_Side for better interpretability

Additional Engineered Features:

Total_Spending: Combined cost of all onboard services

Is_Alone: Indicates if a passenger traveled without family/group

---
##  Exploratory Data Analysis (EDA)

### 1. Univariate Analysis

- Distribution of individual numerical features using:
  - Histogram with KDE overlays (using Plotly)
  - Box plots (to detect outliers)

- Categorical distributions:
  - Count plots for `HomePlanet`, `Destination`, `Cabin_Deck`, etc.

### 2. Bivariate Analysis

- Relationship between `Transported` and:
  - Numerical features via **box + violin plots**
  - Categorical features via **stacked bar charts**
  - KDE overlays (comparison of distributions for `Transported` = 0 vs 1)
  - Grouped bar plots of mean values by class
  - grouped bar input values by class
