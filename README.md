# Kaggle-challenge-group-14

Spaceship Titanic - Predicting Dimensional Transport

The Spaceship Titanic competition challenges you to predict whether a passenger was transported to an alternate dimension during the ship’s collision with a spacetime anomaly. Using detailed personal and transactional records, this project applies the to build a robust machine learning solution.

2.Install requirements:

pip install -r requirements.txt

 Dataset Overview
 Key Features:
**Categorical:** `HomePlanet`, `CryoSleep`, `Cabin`, `Destination`, `VIP`
**Numerical Columns**: Age, RoomService, FoodCourt ,ShoppingMall , Spa , VRDeck
  
## 🔍 Project Overview

### ✅ Goals:
1. Clean and preprocess the raw data.
2. Perform comprehensive Exploratory Data Analysis (EDA).
3. Engineer meaningful features.
4. Prepare data for modeling (splitting, encoding, scaling).
---

## 🧹 Data Cleaning

- **Missing Values** handled through:
  - Group-wise imputations (e.g., median `Age` by group).
  - Domain-based assumptions (e.g., inferring `CryoSleep` from zero expenditure).
- **Cabin Splitting** into:
  - `Cabin_Deck`, `Cabin_Number`, `Cabin_Side`
- **Engineered Features**:
  - `Total_Spending`: Sum of all expenditure columns
  - `Is_Alone`: Boolean indicating solo traveler based on group

---
## 📊 Exploratory Data Analysis (EDA)

### ✅ 1. Univariate Analysis

- Distribution of individual numerical features using:
  - Histogram with KDE overlays (using Plotly)
  - Box plots (to detect outliers)

- Categorical distributions:
  - Count plots for `HomePlanet`, `Destination`, `Cabin_Deck`, etc.
