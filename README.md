# ✈️ Airline Passenger Satisfaction Prediction

## 📌 Project Overview

This project focuses on predicting airline passenger satisfaction using machine learning.

The objective is to classify whether a passenger is satisfied or dissatisfied based on demographic information, flight details, travel class, customer type, and ratings of various airline services.

The project uses **CatBoost Classifier**, a gradient boosting algorithm that handles categorical features effectively.

## 🎯 Objectives

- Explore passenger satisfaction patterns through Exploratory Data Analysis (EDA).
- Identify factors associated with passenger satisfaction.
- Perform data preprocessing and feature analysis.
- Train a CatBoost classification model.
- Evaluate model performance using ROC-AUC.

## 📊 Dataset

The project uses the airline passenger satisfaction dataset provided through the Kaggle competition.

The training dataset contains 699,635 records and 23 columns, including:

- Passenger demographics: Age, Gender.
- Travel information: Flight Distance, Type of Travel, Class.
- Customer information: Customer Type.
- Service ratings: Online Boarding, Seat Comfort, Inflight Entertainment, Food and Drink, etc.
- Flight delays: Departure Delay and Arrival Delay.
- Target variable: `satisfaction`.

## 🔍 Exploratory Data Analysis

The following analyses were performed:

- Dataset structure and data types.
- Missing-value analysis.
- Passenger satisfaction distribution.
- Numerical feature distributions.
- Satisfaction comparison across numerical features.
- Categorical feature analysis using cross-tabulation.
- Relationship between travel type and travel class.
- Departure and arrival delay analysis.

### Key observations

- Personal travel passengers showed considerably lower satisfaction than business travel passengers.
- Business-class passengers generally reported higher satisfaction.
- Online boarding, seat comfort, and inflight entertainment showed notable differences between satisfied and dissatisfied passengers.
- Customer type and travel class were important dimensions to investigate.

## ⚙️ Data Preprocessing

- Removed the passenger `id` column from model features.
- Separated the target variable (`satisfaction`).
- Removed 292 records with missing Arrival Delay values.
- Identified numerical and categorical features.
- Used a stratified train-validation split.

**Dataset split:**
- Training: 80%
- Validation: 20%
- Random state: 42

## 🤖 Model: CatBoost Classifier

CatBoost was selected because it supports categorical features directly without requiring manual one-hot encoding.

### Model configuration

| Parameter | Value |
|---|---:|
| Algorithm | CatBoost Classifier |
| Iterations | 500 |
| Learning Rate | 0.1 |
| Tree Depth | 7 |
| Evaluation Metric | AUC |
| Random Seed | 42 |
| Early Stopping Rounds | 50 |

Categorical features:
- Gender
- Customer Type
- Type of Travel
- Class

## 📈 Model Performance

The model was evaluated on the validation dataset using ROC-AUC.

| Metric | Score |
|---|---:|
| Validation ROC-AUC | **0.957685** |

The result indicates strong discrimination between satisfied and dissatisfied passengers on the validation dataset.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- CatBoost
- Jupyter Notebook


## 🔮 Future Improvements

- Experiment with additional gradient boosting algorithms such as XGBoost and LightGBM.
- Perform hyperparameter optimization.
- Compare different missing-value treatment strategies.
- Analyze feature importance and model explainability.
- Generate predictions for the competition test dataset.
- Prepare and submit the final Kaggle submission file.

## 👨‍💻 Author

**Ayush Naik**

GitHub: [@AHNK-05](https://github.com/AHNK-05)

---

*This project was developed as part of my journey in learning Machine Learning and applying it to real-world classification problems.*
