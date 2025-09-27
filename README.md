Heart Disease Classification: Foundational Model Comparison
Project Overview
This project focuses on comparing the performance of four core machine learning classification algorithms—K-Nearest Neighbors (KNN), Decision Tree, Naive Bayes, and Logistic Regression—to predict the presence of heart disease based on patient data.

The primary goal is to identify the most robust model, prioritizing Recall to minimize False Negatives (missed diagnoses), which is the most critical metric in a medical context.

💾 Dataset
The analysis uses the publicly available Heart Disease dataset, containing 1026 patient records and 13 features (age, sex, chest pain type, resting blood pressure, cholesterol, etc.).

Target Variable: target (1 = Presence of heart disease, 0 = Absence of heart disease).

Data File: heart_diseases.csv

⚙️ Methodology
The analysis was performed in a single, consolidated Jupyter Notebook (Heart_Disease_Classification_Comparison.ipynb) following these steps:

Data Preprocessing: Handled missing values (if any) and checked data distribution.

Train-Test Split: Data was split into 70% training and 30% testing sets (random_state=42) for unbiased evaluation.

Feature Scaling: Standard scaling was applied to all features, a critical step for distance-based and gradient-descent models (like KNN and Logistic Regression).

Model Training & Tuning: Each of the four models was trained and evaluated on the scaled data. The Decision Tree was pruned (max_depth=4) to prevent overfitting.

Evaluation: Performance was measured using Accuracy, Recall, Precision, and F1-Score. Confusion Matrices were generated for visual comparison.

🥇 Model Comparison Summary
The following table summarizes the performance on the unseen Test Set (308 records), ordered by overall accuracy:

Model

Classification Type

Test Accuracy

Recall (Class 1)

False Negatives (FN)

K-Nearest Neighbors (KNN)

Distance-Based

84.7%

0.91

13

Decision Tree (Pruned)

Rule-Based

84.1%

0.88

19

Logistic Regression

Linear Boundary

83.4% (Approx.)

0.85 (Approx.)

23 (Approx.)

Naive Bayes

Probabilistic

81.5%

0.89

16

Champion Model: K-Nearest Neighbors (KNN)
KNN achieved the highest overall accuracy and, most importantly, the highest Recall (0.91) with the lowest number of False Negatives (13). This minimizes the risk of sending a sick patient home with a clean bill of health.

🚀 Next Steps
The next phase of this project will focus on advanced techniques:
Support Vector Machine (SVM): Implement and tune the SVC model to see if non-linear boundaries can outperform KNN.

Ensemble Learning: Introduce models like Random Forest and XGBoost to achieve further gains in predictive stability and accuracy.

Created by Niladri Sanyal

Support Vector Machine (SVM): Implement and tune the SVC model to see if non-linear boundaries can outperform KNN.

Ensemble Learning: Introduce models like Random Forest and XGBoost to achieve further gains in predictive stability and accuracy.
