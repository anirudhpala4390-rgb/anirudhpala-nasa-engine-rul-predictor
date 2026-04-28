# NASA Turbofan Engine Remaining Useful Life Prediction

## Overview

This project predicts the **Remaining Useful Life (RUL)** of turbofan aircraft engines using Machine Learning techniques. By analyzing engine sensor readings and operational settings, the model estimates how many cycles remain before engine failure.

The project demonstrates the concept of **Predictive Maintenance**, helping industries reduce downtime, optimize maintenance schedules, and improve safety.

---

## Problem Statement

Unexpected engine failures can lead to:

- High repair and maintenance costs  
- Unplanned downtime  
- Operational inefficiency  
- Safety risks  

The objective of this project is to build a predictive model that estimates engine life before failure.

---

## Dataset Information

**Source:** NASA CMAPSS Dataset  
**Subset Used:** FD001

### Dataset Includes:

- Engine Unit Number  
- Time Cycles  
- 3 Operational Settings  
- 21 Sensor Measurements  
- Run-to-failure engine records

### Target Variable:

**Remaining Useful Life (RUL)**

RUL = Maximum Cycle - Current Cycle

---

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost / Random Forest  
- Streamlit  
- Pickle  
- Hugging Face Spaces

---

## Project Workflow

### 1. Data Preprocessing

- Loaded dataset  
- Removed unnecessary columns  
- Assigned feature names  
- Handled missing values  
- Created target variable (RUL)

### 2. Feature Engineering

- Selected important sensors  
- Applied MinMax Scaling

### 3. Model Building

Models tested:

- Random Forest Regressor  
- Gradient Boosting Regressor  
- XGBoost Regressor

### Final Model:

Best-performing regression model selected for deployment.

---

## Evaluation Metrics

- MAE (Mean Absolute Error)  
- RMSE (Root Mean Squared Error)  
- R² Score

---

## Deployment

This project is deployed as a **Streamlit Web App**.

### Features:

- User enters engine sensor values  
- Predicts Remaining Useful Life instantly  
- Interactive and simple interface

---

## Folder Structure

```bash
NASA-RUL-Prediction/
│── nasa_model.pkl
│── scaler.pkl
│── requirements.txt
│── Dockerfile
│── README.md
│── src/
│   └── streamlit_app.py
