🩺 Diabetes Prediction System

📌 Project Overview

The Diabetes Prediction System is a Machine Learning project that predicts whether a patient is likely to have diabetes based on health-related attributes. The project emphasizes data preprocessing, exploratory data analysis (EDA), and model evaluation, ensuring practical and reliable results for real-world healthcare applications.

📊 Dataset

- Total Records: 768 patients
- Features: 9 health-related attributes, including:
  - Pregnancies
  - Glucose
  - Blood Pressure
  - Skin Thickness
  - Insulin
  - BMI
  - Diabetes Pedigree Function (DPF)
  - Age
  - Outcome (Target variable: Diabetic/Non-Diabetic)

🔧 Data Preprocessing

- Fixed incorrect/shifted column names.
- Replaced invalid medical values (e.g., Insulin, BMI = 0) with median values.
- Removed extreme outliers using Z-Score.
- Verified no missing or duplicate records.

 📊 Exploratory Data Analysis (EDA)

- Key features strongly linked to diabetes: Pregnancies, Insulin, BMI, and Family History (DPF).
- No severe multicollinearity (correlation < 0.7).
- Significant outliers found in Insulin values.

🤖 Modeling & Results

- Without Hyperparameter Tuning
  - Logistic Regression → 75.58%
  - Decision Tree → 67.46%
  - Random Forest → 77.91%
  - Gradient Boosting → 76.46%
  - SVM → 75.29%
  - Voting Classifier (CV) → 75.89%
  - Stacking → 71.74%
  - XGBoost → 71.01%
  - SMOTE + SVM → 56.52%


 - With Hyperparameter Tuning
  - Model: SMOTE (Synthetic Minority Over-sampling Technique) + XGBoost
  - Validation Strategy: Stratified K-Fold Cross-Validation with GridSearchCV for hyperparameter tuning
  - Test Accuracy: 73.91%


📌 Conclusion

- Logistic Regression, SVC, and KNN are the most reliable models (~80% accuracy).
- Ensemble methods (Voting & Stacking) provide stability but no significant accuracy boost.
- Complex models (Random Forest, Decision Tree, XGBoost) tend to overfit without proper tuning.
- To go beyond 80% accuracy:
  - Advanced feature engineering
  - Better scaling & encoding techniques
  - Improved handling of outliers
 
⚖️ Final Insight

This project demonstrates that simpler models, when combined with proper preprocessing, can perform as well as complex models. Such approaches are practical, efficient, and well-suited for real-world healthcare applications.
