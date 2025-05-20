# Health Insurance Cost Predictor

A web-based application built using Streamlit to predict individual health insurance costs based on various demographic and medical inputs.

## 🧠 Project Overview

This app uses a trained machine learning model to predict insurance costs for individuals based on:
- Age
- Income
- BMI category
- Smoking status
- Medical history
- Genetic risks
- Employment status
- Region
- Insurance plan selected

Two models are used based on age groups:
- `model_young.joblib` for age ≤ 25
- `model_rest.joblib` for age > 25

## 📁 Project Structure

```
.
├── main.py                    # Streamlit frontend UI
├── prediction_helper.py       # Input preprocessing and model prediction logic
└── artifacts/
    ├── model_young.joblib     # Trained model for users aged ≤ 25
    ├── model_rest.joblib      # Trained model for users aged > 25
    ├── scaler_young.joblib    # Scaler for features (age ≤ 25)
    └── scaler_rest.joblib     # Scaler for features (age > 25)
```

## 🚀 How to Run the App

### 1. Install Requirements

```bash
pip install streamlit pandas scikit-learn joblib
```

### 2. Start the Application

```bash
streamlit run main.py
```

## 🧾 Features

- Interactive UI to input user data
- Handles various categorical and numerical fields
- Dynamic model selection based on age
- Feature scaling using predefined scalers
- Normalizes medical risk scores
- Displays predicted insurance cost

## 📌 Input Parameters

The user is prompted to enter the following information:
- **Age**: Integer [18–100]
- **Number of Dependants**: Integer [0–20]
- **Income in Lakhs**: Integer [0–200]
- **Genetical Risk**: Integer [0–5]
- **Insurance Plan**: Bronze / Silver / Gold
- **Employment Status**: Salaried / Self-Employed / Freelancer
- **Gender**: Male / Female
- **Marital Status**: Married / Unmarried
- **BMI Category**: Normal / Overweight / Obesity / Underweight
- **Smoking Status**: No Smoking / Occasional / Regular
- **Region**: Northwest / Southeast / Northeast / Southwest
- **Medical History**: Multiple combinations (e.g., Diabetes & Heart disease)

## ⚙️ Model and Preprocessing Details

- Preprocessing encodes categorical fields and scales numerical ones.
- Medical history is converted into a normalized risk score based on predefined weights.
- Inputs are transformed using the appropriate scaler (`scaler_young` or `scaler_rest`).
- Models return the estimated insurance cost.

## 📩 Contact

Created as part of the [Projects Portfolio](https://codebasics.io/).  
All rights reserved to Murali Krishna at reachmurali2@gmail.com

---

> ✨ Feel free to contact me for further queries!
