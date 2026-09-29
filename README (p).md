# Household Energy Consumption Prediction

## 📌 Project Overview

This project focuses on predicting **household energy consumption** using Machine Learning. The dataset contains household-related and environmental features that can influence electricity consumption.

A **Polynomial Regression** model is developed to predict `Energy_Consumption_kWh` based on:

* Household Size
* Average Temperature
* Peak Hours Usage

The project also evaluates the model using standard regression metrics and compares the actual and predicted energy consumption.

---

## 🎯 Objective

The main objective of this project is to build a Machine Learning model that can predict household energy consumption based on selected input features.

The project includes:

* Loading and exploring the dataset
* Checking the structure and characteristics of the data
* Handling missing values
* Selecting relevant features
* Splitting the dataset into training and testing sets
* Applying Polynomial Feature Transformation
* Building a Linear Regression model
* Making predictions
* Evaluating model performance
* Comparing actual and predicted values visually

---

## 📂 Dataset

The dataset used in this project is:

**`household_energy_consumption.csv`**

The target variable is:

`Energy_Consumption_kWh`

### Features Used

| Feature                  | Description                                  |
| ------------------------ | -------------------------------------------- |
| `Household_Size`         | Number of people in the household            |
| `Avg_Temperature_C`      | Average temperature in Celsius               |
| `Peak_Hours_Usage_kWh`   | Energy usage during peak hours               |
| `Energy_Consumption_kWh` | Total energy consumption and target variable |

---

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab / Jupyter Notebook

---

## 🤖 Machine Learning Algorithm

### Polynomial Regression

Polynomial Regression is used to model the relationship between the input variables and household energy consumption.

The project uses:

```python
PolynomialFeatures(degree=2)
```

The polynomial features are then passed to a:

```python
LinearRegression()
```

model.

### Model Workflow

```text
Dataset
   ↓
Data Exploration
   ↓
Missing Value Handling
   ↓
Feature Selection
   ↓
Train-Test Split
   ↓
Polynomial Feature Transformation
   ↓
Linear Regression Model
   ↓
Prediction
   ↓
Model Evaluation
```

---

## 🔍 Data Preprocessing

The dataset is explored using:

* `head()`
* `tail()`
* `shape`
* `info()`
* `describe()`
* `dtypes`
* `columns`
* `isnull().sum()`

Missing values are handled using:

```python
df = df.dropna()
```

---

## 📊 Feature Selection

The following features are used as independent variables:

```python
X = df[[
    "Household_Size",
    "Avg_Temperature_C",
    "Peak_Hours_Usage_kWh"
]]
```

The target variable is:

```python
y = df["Energy_Consumption_kWh"]
```

---

## 📚 Train-Test Split

The dataset is divided into training and testing data using an **80:20 split**.

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

* **80%** → Training data
* **20%** → Testing data

---

## 📈 Model Evaluation

The model is evaluated using the following regression metrics:

### Mean Absolute Error (MAE)

Measures the average absolute difference between actual and predicted values.

### Mean Squared Error (MSE)

Measures the average squared difference between actual and predicted values.

### Root Mean Squared Error (RMSE)

The square root of MSE, which represents prediction error in the same unit as energy consumption.

### R² Score

Measures how well the model explains the variation in the target variable.

The notebook calculates:

```python
MAE
MSE
RMSE
R²
```

---

## 📋 Actual vs Predicted Values

The project creates a comparison between the actual and predicted energy consumption values.

```python
result = pd.DataFrame({
    "Actual Energy": y_test.values,
    "Predicted Energy": y_pred
})
```

This helps evaluate how closely the model's predictions match the actual household energy consumption.

---

## 📊 Visualization

A scatter plot is created to compare:

* **X-axis:** Actual Energy Consumption
* **Y-axis:** Predicted Energy Consumption

The visualization helps understand the relationship between the actual and predicted values.

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-link>
```

### 2. Open the Notebook

Open:

```text
ML_task_4.ipynb
```

using:

* Google Colab
* Jupyter Notebook
* VS Code

### 3. Add the Dataset

Make sure the following dataset is available:

```text
household_energy_consumption.csv
```

### 4. Install Required Libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### 5. Run the Notebook

Execute the cells in order to perform data preprocessing, model training, prediction, and evaluation.

---

## 📁 Project Structure

```text
Household-Energy-Consumption/
│
├── ML_task_4.ipynb
├── household_energy_consumption.csv
└── README.md
```

---

## 💡 Key Learning Outcomes

Through this project, the following Machine Learning concepts were practiced:

* Data loading using Pandas
* Exploratory Data Analysis
* Missing value handling
* Feature selection
* Train-test splitting
* Polynomial feature transformation
* Linear Regression
* Model prediction
* Regression evaluation metrics
* Actual vs predicted visualization

---

## 🔮 Future Improvements

The project can be further improved by:

* Comparing Polynomial Regression with other regression algorithms
* Performing more detailed Exploratory Data Analysis
* Testing different polynomial degrees
* Applying feature scaling where appropriate
* Performing hyperparameter tuning
* Adding more relevant household and environmental features
* Deploying the model as a simple web application

---

## 👩‍💻 Author

**Ayyanar Kanna .P**

BCA Student | Aspiring Full Stack Developer & Data Analyst
