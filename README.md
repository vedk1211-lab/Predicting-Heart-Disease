❤️ Predicting Heart Disease

Kaggle Playground Series 2026 – Season 6 Episode 2

This repository contains my solution to the Kaggle competition:

“Predicting Heart Disease”
Part of the 2026 Tabular Playground Series.

📌 Competition Overview

Host: Kaggle

Competition: Playground Series S6E2

Start Date: February 1, 2026

Final Submission Deadline: February 28, 2026

Evaluation Metric: ROC-AUC

Problem Type: Binary Classification

The objective is to predict the probability that a patient has heart disease using clinical and demographic features.
---
🎯 Problem Statement

Given patient-related attributes (e.g., medical indicators, health measurements, and demographic factors), build a machine learning model that predicts the likelihood of heart disease.

Target variable:

Heart Disease → Binary (0 = No, 1 = Yes)

Submissions must contain predicted probabilities for each test id.
---
📂 Dataset Structure

train.csv → Training data (features + target)

test.csv → Test data (features only)

sample_submission.csv → Submission format

Submission Format
id,Heart Disease
630000,0.2
630001,0.3
630002,0.1


The prediction must be a probability, not a class label.
---
📊 Evaluation Metric

Submissions are evaluated using:

ROC-AUC (Area Under the Receiver Operating Characteristic Curve)

Why ROC-AUC?

Measures how well the model distinguishes between the two classes.

Threshold-independent metric.

Ideal for probability-based classification problems.

Higher ROC-AUC → Better class separation.
---
⚙️ Approach
1️⃣ Data Preprocessing

Checked for missing values

Encoded categorical variables

Feature scaling (if required)

Stratified K-Fold Cross Validation

2️⃣ Model Used

Gradient Boosting (LightGBM / XGBoost / CatBoost)

Early stopping to prevent overfitting

Probability-based predictions

3️⃣ Cross-Validation Strategy

Stratified K-Fold

Evaluated using ROC-AUC

Averaged predictions across folds
---
🚀 How to Run (Kaggle Notebook)
train = pd.read_csv("/kaggle/input/playground-series-s6e2/train.csv")
test = pd.read_csv("/kaggle/input/playground-series-s6e2/test.csv")


After training:

submission.to_csv("submission.csv", index=False)


Download from the Output section or submit directly from the notebook.
---
🧠 Potential Improvements

Hyperparameter tuning (Optuna)

Feature interaction engineering

Ensemble models

Stacking multiple boosting models

SHAP explainability analysis

Calibration of predicted probabilities
---

🏁 Results

Cross-Validation ROC-AUC: [Add your score]

Kaggle Public Leaderboard Score: [Add score]

Kaggle Private Leaderboard Score: [Add score]


---
Link

https://www.kaggle.com/code/vedantkulka12/notebook520fb53bc3
