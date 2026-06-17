# 🏠 House Price Prediction System

An end-to-end Machine Learning project that predicts California housing prices using demographic, geographic, and housing-related features. The project demonstrates a complete ML workflow including Exploratory Data Analysis (EDA), data preprocessing, feature engineering, model selection, cross-validation, hyperparameter tuning, evaluation, and inference.

---

## 📌 Project Overview

Accurately estimating house prices is a critical problem in the real-estate industry. In this project, multiple regression models are trained and compared to predict median house values using the California Housing dataset.

The project follows a production-oriented machine learning workflow:

```text
EDA
   ↓
Data Cleaning
   ↓
Preprocessing Pipeline
   ↓
Baseline Model
   ↓
Cross Validation
   ↓
Model Selection
   ↓
Hyperparameter Tuning
   ↓
Final Evaluation
   ↓
Prediction System
```

---

## 🎯 Objectives

- Perform Exploratory Data Analysis (EDA)
- Handle missing values systematically
- Build reusable preprocessing pipelines
- Compare multiple machine learning models
- Use K-Fold Cross Validation for reliable evaluation
- Optimize the best model using GridSearchCV
- Evaluate model performance using multiple regression metrics
- Build a reusable house price prediction system

---

## 📊 Dataset

### California Housing Dataset

The dataset contains information collected from California districts and includes demographic, geographical, and housing-related attributes.

### Dataset Size

- Rows: 20,640
- Features: 9
- Target Variable: 1

### Features

| Feature | Description |
|----------|-------------|
| longitude | Geographic longitude |
| latitude | Geographic latitude |
| housing_median_age | Median age of houses |
| total_rooms | Total rooms in the district |
| total_bedrooms | Total bedrooms |
| population | Population of the district |
| households | Number of households |
| median_income | Median income of residents |
| ocean_proximity | Proximity to the ocean (categorical) |

### Target Variable

```text
median_house_value
```

The median value of houses in a district.

---

## 🔍 Exploratory Data Analysis

The project includes extensive EDA to understand the structure and quality of the dataset.

### Analysis Performed

- Dataset overview
- Data types inspection
- Missing value analysis
- Duplicate detection
- Descriptive statistics
- Distribution analysis
- Outlier analysis
- Correlation analysis
- Feature-target relationships

### Visualizations

- Histograms
- Count Plots
- Box Plots
- Correlation Heatmaps
- Target Distribution Analysis
- Residual Analysis

### Key Findings

- Dataset contains both numerical and categorical features.
- Only `total_bedrooms` contains missing values.
- Target variable shows slight skewness.
- Median income has a strong correlation with house prices.
- Several geographical features significantly influence housing prices.

---

## ⚙️ Data Preprocessing

A reusable preprocessing pipeline was built using Scikit-Learn.

### Numerical Features

- Missing Value Imputation
- Standard Scaling

### Categorical Features

- Missing Value Handling
- One-Hot Encoding

### Pipeline Components

```python
SimpleImputer
StandardScaler
OneHotEncoder
ColumnTransformer
Pipeline
```

This ensures consistent preprocessing during both training and inference.

---

## 🤖 Models Evaluated

The following regression models were trained and compared:

### 1. Linear Regression

Used as the baseline model.

### 2. Ridge Regression

Linear model with L2 regularization.

### 3. Lasso Regression

Linear model with L1 regularization.

### 4. Random Forest Regressor

Ensemble learning method using multiple decision trees.

### 5. HistGradientBoostingRegressor

Gradient boosting model optimized for large datasets.

---

## 📈 Model Evaluation

### Evaluation Metrics

The models were evaluated using:

- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- R² Score

### Cross Validation Strategy

```python
KFold Cross Validation
n_splits = 5
shuffle = True
```

This reduces evaluation bias and provides more reliable performance estimates.

---

## 🏆 Best Model

### HistGradientBoostingRegressor

The HistGradientBoostingRegressor achieved the best cross-validation performance and was selected for final optimization.

Reasons:

- Strong generalization ability
- Excellent handling of nonlinear relationships
- Robust performance on tabular datasets
- Superior RMSE compared to other models

---

## 🔧 Hyperparameter Tuning

The best model was optimized using:

```python
GridSearchCV
```

### Tuned Parameters

- learning_rate
- max_depth
- max_leaf_nodes
- min_samples_leaf
- l2_regularization

Grid Search was performed using 5-Fold Cross Validation and RMSE as the optimization metric.

---

## 📉 Final Evaluation

The optimized model was evaluated on both:

- Training Dataset
- Test Dataset

Metrics reported:

```text
RMSE
MAE
R² Score
```

Additional diagnostics:

- Residual Analysis
- Prediction Error Inspection

These evaluations help verify that the model generalizes well and is not significantly overfitting.

---

## 🚀 Predictive System

A reusable prediction function was developed that accepts housing attributes and returns the estimated house value.

### Example Inputs

- Longitude
- Latitude
- Housing Median Age
- Total Rooms
- Total Bedrooms
- Population
- Households
- Median Income
- Ocean Proximity

### Output

```text
Predicted House Price
```

This makes the project easily extensible for deployment through:

- Flask
- FastAPI
- Streamlit
- Spring Boot APIs
- Cloud Platforms

---

## 🛠️ Technologies Used

### Programming Language

- Python

### Data Analysis

- Pandas
- NumPy

### Visualization

- Matplotlib
- Seaborn

### Machine Learning

- Scikit-Learn

### Model Selection & Optimization

- Cross Validation
- KFold
- GridSearchCV

---

## 📂 Project Structure

```text
House_Price_Prediction_System/
│
├── housing.csv
├── House_Price_Prediction.ipynb
├── README.md
│
└── outputs/
    ├── visualizations
    ├── model_results
    └── evaluation_plots
```

---

## 💡 Future Improvements

Potential enhancements include:

### Feature Engineering

- Rooms per Household
- Bedrooms per Room
- Population per Household

### Advanced Modeling

- XGBoost
- LightGBM
- CatBoost

### Data Transformations

- Log Transformation of Target Variable
- Robust Scaling
- Outlier Treatment

### Deployment

- Streamlit Web Application
- FastAPI REST Service
- Docker Containerization
- Cloud Deployment

---

## 📚 Learning Outcomes

Through this project, I gained practical experience with:

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Engineering
- Machine Learning Pipelines
- Cross Validation
- Hyperparameter Optimization
- Ensemble Learning
- Regression Evaluation Metrics
- Building End-to-End ML Systems

---

## ⭐ Project Highlights

✅ End-to-End Machine Learning Workflow

✅ Comprehensive Exploratory Data Analysis

✅ Production-Ready Preprocessing Pipeline

✅ Comparison of Multiple ML Models

✅ Cross Validation Based Model Selection

✅ Hyperparameter Tuning with GridSearchCV

✅ Ensemble Learning using HistGradientBoosting

✅ Reusable House Price Prediction System

---