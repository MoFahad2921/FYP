# Capstone 2 – SystemLink Fuel Burn Prediction Model

## Overview

This project is a **final year capstone machine learning model** focused on **predicting aircraft fuel burn** based on operational and environmental flight parameters. The notebook builds an end-to-end predictive pipeline: data loading, feature engineering, target variable creation, model training, and performance comparison across multiple regression algorithms.

The goal is to demonstrate how flight operational data can be used to **estimate and predict fuel consumption**, supporting analytics use cases such as operational efficiency, cost optimization, and decision support systems (e.g., SystemLink-style monitoring platforms).

---

## Key Objectives

* Preprocess and analyze flight operations data
* Engineer a realistic fuel burn target variable
* Simulate real-world noise in fuel consumption
* Train and compare multiple regression models
* Evaluate model performance using standard ML metrics

---

## Dataset

The notebook loads a flight operations dataset from **Google Drive** (Excel format):

```
flight_ops_dataset_upgraded.xlsx
```

### Example Input Features

* `flight_distance_nm`
* `taxi_time_min`
* `holding_time_min`
* `payload_weight_kg`
* `wind_component_knots`
* `cruise_altitude_ft`
* `apu_usage_min`

> ⚠️ **Note:** The dataset path is hardcoded for Google Colab usage. Update the path if running locally.

---

## Target Variable Engineering

Two fuel burn variables are created:

### 1. Estimated Fuel Burn

A calculated fuel burn value based on domain-inspired heuristics:

* Distance-based burn
* Taxi and holding penalties
* Payload impact
* Wind and cruise altitude adjustments
* APU usage impact

### 2. Real Fuel Burn (Simulated)

To mimic real-world uncertainty, Gaussian noise (±6%) is added:

* Creates a more realistic prediction task
* Serves as the model target variable

---

## Machine Learning Models

The notebook trains and evaluates multiple regression models, including:

* **Linear Regression**
* **Lasso Regression**
* **Ridge Regression**
* **Random Forest Regressor**
* **XGBoost Regressor**

Each model is trained using a **train-test split** and evaluated using consistent metrics for fair comparison.

---

## Evaluation Metrics

Model performance is assessed using:

* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score (Coefficient of Determination)**

These metrics provide insight into prediction accuracy, error magnitude, and explanatory power.

---

## Other Techniques Used

In addition to supervised regression models, the project also explores:

* **Clustering** – to identify patterns and groupings within flight operations data
* **Association Rule Mining** – to discover relationships between operational variables

These techniques provide supplementary insights beyond fuel burn prediction, supporting exploratory data analysis and decision-making.

---

## Project Workflow

1. Load and inspect dataset
2. Feature selection and preprocessing
3. Target variable creation
4. Noise simulation for realism
5. Exploratory analysis using clustering and association rules
6. Model training and prediction
7. Performance comparison and analysis

---

## Requirements

Install the following Python libraries:

```bash
pip install pandas numpy scikit-learn openpyxl
```

The notebook is designed to run smoothly on **Google Colab**.

---

## How to Run

1. Upload the dataset to Google Drive
2. Mount Google Drive in Colab
3. Open the notebook using the Colab badge
4. Run cells sequentially from top to bottom

---

## Future Improvements

* Add neural network regression models
* Hyperparameter tuning
* Real-world fuel burn dataset integration
* Deployment as a SystemLink or dashboard service

---

## Author

Fahad Iqbal

---

## License

This project is for **academic and educational purposes** only.
