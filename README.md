# Spaceship Titanic Prediction with Feature Engineering and Ensemble Learning

## 1. Project Overview

This project is based on the Kaggle Spaceship Titanic competition. The goal is to predict whether a passenger was transported to an alternate dimension based on demographic information, cabin information, group information, family information, and spending behavior.

This is a binary classification machine learning project. It covers the full workflow of a Kaggle-style tabular data competition, including data preprocessing, exploratory data analysis, feature engineering, model training, cross-validation, ensemble learning, threshold tuning, post-processing, and submission file generation.

## 2. Repository Contents

This repository contains the following files and folders:

* source_notebook.ipynb
  Main notebook for data preprocessing, feature engineering, model training, validation, ensemble learning, threshold tuning, and submission generation.

* requirements.txt
  Required Python packages.

* Dataset_Link.txt
  Dataset source and download instructions.

* submissions/
  Generated Kaggle submission files.

* report/Report.pdf  
  Final project report, including data analysis, methodology, experiments, results, and conclusions.

## 3. Dataset

The dataset comes from the Kaggle Spaceship Titanic competition.

The original dataset files are not included in this repository. To run the notebook, please download the following files from Kaggle:

* train.csv
* test.csv
* sample_submission.csv

Place these files in the same folder as source_notebook.ipynb before running the notebook.

## 4. Feature Engineering

The project includes several feature engineering steps for structured tabular data, including:

* PassengerId parsing
* GroupId and GroupSize extraction
* Solo passenger indicator
* CabinDeck, CabinNum, and CabinSide extraction
* TotalSpend and NoSpend features
* Spending behavior features
* Surname and family-related features
* HomePlanet and Destination interaction features
* Group-level post-processing features

## 5. Models

The project experiments with multiple machine learning models, including:

* Logistic Regression
* ExtraTrees
* HistGradientBoosting
* LightGBM
* CatBoost

The final prediction system mainly uses ensemble learning to combine the strengths of multiple models.

## 6. Validation Strategy

The project uses Stratified K-Fold cross-validation to evaluate model performance. Out-of-fold predictions are used for model comparison, threshold tuning, and ensemble evaluation.

This validation strategy helps reduce overfitting to the public leaderboard and provides a more stable estimate of model performance.

## 7. Final Result

Best observed public Kaggle leaderboard score:

0.81248

Ranking snapshot:

#248

## 8. How to Run

Install the required packages:

pip install -r requirements.txt

Download the Kaggle dataset and place train.csv, test.csv, and sample_submission.csv in the same folder as source_notebook.ipynb.

Then open and run:

source_notebook.ipynb

The notebook will perform preprocessing, feature engineering, model training, validation, ensemble prediction, threshold tuning, and submission file generation.

## 9. Key Takeaways

This project shows that strong feature engineering is very important for tabular machine learning tasks. Group, cabin, family, and spending-related features provided useful predictive signals.

The final ensemble model improved robustness by combining models with different strengths and error patterns. This project demonstrates a complete machine learning workflow for a Kaggle-style classification problem.
