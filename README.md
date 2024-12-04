# ML-project-CAR-Price
# Car Price Prediction Project

## Project Description
This project aims to analyze the factors influencing car prices in the US market. A Chinese automobile company is entering the US market and needs to understand how car prices are determined to design competitive models and strategies. By building predictive models using machine learning techniques, this project identifies the most significant factors affecting car prices and provides insights into pricing dynamics.

---

## Objectives
1. **Identify Significant Variables:** Understand the factors that influence car prices.
2. **Build Predictive Models:** Use machine learning models to predict car prices based on available data.
3. **Analyze Feature Importance:** Highlight the features with the most significant impact on price.
4. **Optimize Models:** Perform hyperparameter tuning to achieve better predictions.

---

## Dataset
- **Source:** Provided by the consulting firm based on market surveys.
- **Size:** 205 rows and 26 columns.
- **Target Variable:** `price`
- **Features:** 
  - Numerical: Engine size, horsepower, dimensions, etc.
  - Categorical: Fuel type, body style, etc.

---

## Methodology

### 1. Data Preprocessing
- **Cleaning:** Handled missing or erroneous data.
- **Feature Transformation:**
  - Numerical features: Standardized using `StandardScaler`.
  - Categorical features: One-hot encoded using `OneHotEncoder`.
- **Data Split:** Divided into training (80%) and test (20%) datasets.

### 2. Model Implementation
Built and evaluated the following machine learning models:
1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. Gradient Boosting Regressor
5. Support Vector Regressor (SVR)

### 3. Model Evaluation
Metrics used to evaluate model performance:
- **R-squared:** Measures goodness of fit.
- **Mean Squared Error (MSE):** Penalizes larger errors.
- **Mean Absolute Error (MAE):** Averages the absolute prediction errors.

### 4. Feature Importance Analysis
Feature importance was extracted from tree-based models (e.g., Random Forest and Gradient Boosting) to identify the most influential variables affecting car prices.

### 5. Hyperparameter Tuning
Hyperparameter optimization for Random Forest was performed using `GridSearchCV` to improve model performance.

---

## Results
### Model Evaluation Metrics
| Model                     | MSE           | MAE          | R-squared |
|---------------------------|---------------|--------------|-----------|
| **Linear Regression**      | 10,067,310    | 2244.60      | 0.872     |
| **Decision Tree Regressor**| 8,223,687     | 1847.43      | 0.896     |
| **Random Forest Regressor**| 3,337,152     | 1276.40      | 0.958     |
| **Gradient Boosting Regressor** | 5,786,643  | 1666.40      | 0.927     |
| **Support Vector Regressor**| 86,811,860   | 5694.47      | -0.099    |

- **Best Model:** Random Forest Regressor with an R-squared of 0.96 and the lowest error metrics.

### Feature Importance
- Significant features influencing car price:
  1. Engine size
  2. Horsepower
  3. Curb weight
  4. Width
  5. Drive wheel type

### Hyperparameter Tuning Results
- **Best Parameters:**  
  - `n_estimators`: 200  
  - `max_depth`: 20  
  - `min_samples_split`: 2  
  - `min_samples_leaf`: 1  
- **R-squared after tuning:** 0.965 (slight improvement).

---

## Technologies Used
- **Programming Language:** Python
- **Libraries:** 
  - `pandas`, `numpy` for data manipulation.
  - `sklearn` for machine learning models and preprocessing.
  - `matplotlib`, `seaborn` for visualizations.

---

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <project-folder>
