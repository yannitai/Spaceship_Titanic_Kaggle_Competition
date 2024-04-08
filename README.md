# Spaceship Titanic Kaggle Competition

## Overview
This project is based on the Kaggle competition - [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic/overview). The goal is to predict whether passengers aboard the spaceship Titanic during its collision were transported to an alternate dimension.
* The target variable for predictions is `Transported`.

## Dataset
The dataset is divided into train and test sets with passenger information like name, cabin, and expenses on the spaceship.

## Exploratory Data Analysis (EDA)
- Distribution and count of the 'Transported' target variable.
- Identification of missing values across features.
- Visualization of data distributions and relationships among features.

## Data Preprocessing
- Missing values are addressed by imputation techniques.
- Binary variables like 'CryoSleep' are transformed into numerical.
- Categorical variables are one-hot encoded for model compatibility.

## Feature Engineering
- New features like total expenses are created by summing individual expenses.
- Interaction terms are considered to capture the combined effect of features.

## Statistical Inference
- Two-sample t-tests are performed to check for mean differences between groups, particularly focusing on the 'Transported' status against other features.

## Machine Learning Models
Multiple models are trained and validated:
- Logistic Regression
- Random Forest Classifier
- Support Vector Machine Classifier
- XGBoost Classifier
- Gradient Boosting Classifier

## Ensemble Techniques
- VotingClassifier combines predictions from the individual models using a 'hard' or 'soft' voting strategy.
- StackingClassifier stacks the individual models and uses a final estimator to make the prediction.

## Model Tuning and Evaluation
- Hyperparameters are tuned using GridSearchCV for optimal performance.
- Model performance is assessed using accuracy, and the best models are identified based on their cross-validation scores.

## Kaggle Competition Submission
The best model is used to predict the 'Transported' status of passengers in the test set, and the predictions are submitted to the Kaggle competition.

## Results
The highest Kaggle accuracy achieved is 0.8034 with a VotingClassifier ensemble method.

## Repository Structure
- `train.csv` - the training set
- `test.csv` - the test set
- `sample_submission.csv` - a sample submission file in the correct format
- `main.ipynb` - Jupyter notebook with all the analysis and model building


