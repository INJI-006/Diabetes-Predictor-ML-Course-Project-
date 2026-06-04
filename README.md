# Diabetes Prediction using Machine Learning

## 🔍 Project Question
Can we predict whether a patient has diabetes based on clinical and demographic features (HbA1c, blood glucose, BMI, age, hypertension, heart disease, smoking history)?

## 📊 Dataset
- Source: Diabetes prediction dataset (Kaggle-style)
- Size: 100,000 rows → cleaned to 95,586 rows
- Features: gender, age, hypertension, heart_disease, smoking_history, bmi, HbA1c_level, blood_glucose_level, diabetes (target)

## 🧹 Data Cleaning
- Removed duplicates
- Replaced 'No Info' in smoking_history with mode
- Filtered invalid genders
- Capped BMI at 60
- Converted age to integer

## 🔬 Feature Engineering & Selection
- Created 4 new features: age_group, bmi_category, glucose_risk, risk_score
- Used SelectKBest (chi²) to select top 8 features

## 🤖 Models Compared
- Logistic Regression
- Random Forest (selected)
- Gradient Boosting

## ⚙️ Hyperparameter Tuning
- GridSearchCV (3‑fold CV) on Random Forest
- Best params: n_estimators=200, max_depth=20, min_samples_split=2

## ✅ Final Performance (Tuned Random Forest)
- Accuracy: 0.973
- Precision: 0.936
- Recall: 0.951
- F1-score: 0.943

## 🌐 Live Web App
Try it yourself:  
(https://pp2gcxmicxjsajkvjykyfw.streamlit.app/)

## 📁 Repository Structure
