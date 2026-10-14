# 🚗 Auto Price Prediction using Machine Learning

## 📌 Project Overview

This project focuses on **predicting automobile prices using Machine Learning**. The Auto dataset contains different features related to automobiles such as wheel-base, length, width, height, curb-weight, engine-size, horsepower, city-mpg, highway-mpg, and other vehicle characteristics.

In this project, **Decision Tree Regression** is used to predict the price of an automobile. The dataset is preprocessed, missing values are handled, and the model is evaluated using different regression performance metrics.

---

## 🎯 Objectives

- To understand and preprocess the Auto dataset.
- To handle missing values in the dataset.
- To convert categorical/numerical data into suitable formats.
- To select relevant features for prediction.
- To train a Decision Tree Regression model.
- To evaluate the model using regression metrics.
- To perform hyperparameter tuning for improving model performance.

---

## 📂 Dataset

The project uses an **Auto dataset** containing:

- **205 records**
- **26 original columns**
- Automobile specifications and price information.

### Important Features

- Symboling
- Wheel Base
- Length
- Width
- Height
- Curb Weight
- Number of Cylinders
- Engine Size
- Compression Ratio
- Horsepower
- Peak RPM
- City MPG
- Highway MPG
- Price

The target variable is:

**`price`**

---

## 🔧 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Replaced `?` values with `NaN`.
3. Converted the number of cylinders from words into numerical values.
4. Removed selected categorical columns that were not used for modelling.
5. Converted `price`, `horsepower`, and `peak-rpm` into floating-point values.
6. Checked for missing values.
7. Filled missing values using the mean of the respective columns.
8. Separated the features (`X`) and target variable (`y`).
9. Split the dataset into training and testing sets using an **80:20 ratio**.

---

## 🤖 Machine Learning Model

### Decision Tree Regression

A **Decision Tree Regressor** was used to predict automobile prices.

```python
from sklearn.tree import DecisionTreeRegressor

dt_reg = DecisionTreeRegressor()
dt_reg.fit(X_train, y_train)
```

The trained model is then used to predict prices for both training and testing datasets.

---

## 📊 Model Evaluation

The following metrics were used:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

### Test Data Performance

| Metric | Result |
|---|---:|
| MSE | 6,061,483.23 |
| RMSE | 2,462.01 |
| MAE | 1,718.75 |
| R² Score | **0.9223** |

### Training Data Performance

| Metric | Result |
|---|---:|
| MSE | 225,952.92 |
| RMSE | 475.35 |
| MAE | 106.81 |
| R² Score | **0.9961** |

The Decision Tree model achieved an **R² score of approximately 92.23% on the test dataset**, indicating good predictive performance.

---

## ⚙️ Hyperparameter Tuning

Hyperparameter tuning was also explored to improve the performance of the Decision Tree model.

The project uses:

- `GridSearchCV`
- `RandomizedSearchCV`

Parameters such as the **splitter** and other Decision Tree parameters can be tuned to obtain a better-performing model.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

## 📁 Project Structure

```text
Auto-Price-Prediction/
│
├── autos_dataset.csv
├── Day 60_Decision Tree Linear regression_Auto Data Set.ipynb
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
```

### 2. Open the project folder

```bash
cd Auto-Price-Prediction
```

### 3. Install required libraries

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebook

Open the `.ipynb` file and run the cells sequentially.

---

## 📈 Results

The Decision Tree Regression model performed well on the Auto dataset.

The model achieved:

**Test R² Score: 0.9223**

This means the model explains approximately **92.23% of the variation in automobile prices** on the test data.

---

## 🔮 Future Scope

- Compare Decision Tree with Linear Regression, Random Forest, and other regression algorithms.
- Perform advanced feature engineering.
- Use cross-validation for better model evaluation.
- Optimize hyperparameters further.
- Build a user-friendly web application using **Streamlit**.
- Allow users to enter automobile specifications and get predicted prices.
