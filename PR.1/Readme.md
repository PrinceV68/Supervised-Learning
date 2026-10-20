<div align="center">

# 🏡 House Price Prediction

### ✨ Predictive Insight Engine · Supervised Learning

**Turning property data into useful price insights with Python and machine learning.**

<p>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Machine%20Learning-Regression-7C3AED?style=for-the-badge" alt="Machine Learning Regression">
  <img src="https://img.shields.io/badge/Notebook-Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Notebook">
  <img src="https://img.shields.io/badge/Status-Learning%20Project-16A34A?style=for-the-badge" alt="Learning Project">
</p>

---

</div>

## 🧭 Table of Contents

- [🌟 About the Project](#-about-the-project)
- [🎯 Project Objectives](#-project-objectives)
- [📦 Dataset Overview](#-dataset-overview)
- [🛠️ Tools and Technologies](#️-tools-and-technologies)
- [🧪 Project Workflow](#-project-workflow)
- [📈 Models and Evaluation](#-models-and-evaluation)
- [📊 Metrics Explained](#-metrics-explained)
- [🚀 Getting Started](#-getting-started)
- [📁 Project Structure](#-project-structure)
- [🔎 Key Questions Explored](#-key-questions-explored)
- [💡 Possible Improvements](#-possible-improvements)
- [⚠️ Limitations](#️-limitations)
- [👨‍💻 Author](#-author)
- [👤 Project Details](#-project-details)

---

## 🌟 About the Project

House prices can depend on many things: the size of the property, the number of bedrooms and bathrooms, its location, age, and extra features. This project uses a house-price dataset to explore those relationships and build regression models that estimate a property's price.

The notebook follows a practical machine-learning workflow: prepare the data, visualize useful patterns, train different models, compare their predictions, and review the results. It also includes a from-scratch comparison of gradient-descent approaches.

> 💬 **The main idea:** learn how different regression methods use property features to estimate house prices—and how to check whether their predictions are useful.

## 🎯 Project Objectives

- 🧹 **Prepare the data** by checking its structure and handling missing values.
- 🔍 **Explore patterns** between property features and house prices.
- 📐 **Build simple linear regression** using `area_sqft`.
- 🧩 **Build multiple linear regression** using several property features.
- 🌱 **Test polynomial regression** with degree 2 and degree 3.
- ⚙️ **Implement gradient descent** using Batch, Stochastic, and Mini-Batch updates.
- 📏 **Evaluate models** using common regression metrics.
- 🧠 **Review model fit** and discuss possible overfitting or underfitting.

## 📦 Dataset Overview

**Dataset file:** `RealEstate_HousePrice_Dataset_4200.xlsx`

The dataset contains property information and a price column used as the prediction target. The following fields are used to understand and model house prices:

| 🏷️ Column | 📝 Meaning |
|---|---|
| `house_id` | Unique identifier for each house |
| `area_sqft` | House area in square feet |
| `bedrooms` | Number of bedrooms |
| `bathrooms` | Number of bathrooms |
| `location_score` | Numeric score representing the location |
| `age_years` | Age of the house in years |
| `distance_city_km` | Distance from the city in kilometres |
| `lot_size_sqft` | Plot size in square feet |
| `has_garage` | Indicates whether a garage is available |
| `has_pool` | Indicates whether a pool is available |
| `renovation_years_ago` | Number of years since renovation |
| `house_price_inr` | House price in Indian rupees; prediction target |

### 🎯 Target and Features

- **Target (`y`):** `house_price_inr`
- **Possible input features (`X`):** property area, bedrooms, bathrooms, location score, age, distance, lot size, garage, pool, and renovation timing.
- **Identifier note:** `house_id` identifies a record; it should not be treated as a meaningful property feature.

*Use the feature columns actually selected in the notebook when interpreting its results.*

## 🛠️ Tools and Technologies

| Tool | How it is used |
|---|---|
| 🐍 **Python** | Main programming language |
| 🧮 **Pandas** | Load and inspect tabular data |
| 🔢 **NumPy** | Numerical calculations |
| 📉 **Matplotlib** | Create plots and model visualizations |
| 🎨 **Seaborn** | Explore relationships in the data |
| 🤖 **Scikit-learn** | Split data, train regression models, and calculate metrics |
| 📓 **Jupyter Notebook** | Run code step by step and document the workflow |
| 📂 **OpenPyXL** | Read Excel files through Pandas |

## 🧪 Project Workflow

### 1. 🧹 Data Preparation

Load the Excel dataset, inspect the rows and columns, check for missing values, and prepare the input features and target variable.

### 2. 📊 Exploratory Data Analysis

Use plots to look at the relationship between `area_sqft` and `house_price_inr`. Visual checks help reveal broad patterns and unusual observations before fitting a model.

### 3. ✂️ Train-Test Split

Separate the data into training and testing sets. The training set is used to fit the model; the test set helps check how it performs on data it has not seen during training.

### 4. 📐 Simple Linear Regression

Train a model using `area_sqft` as the single input feature. Review its slope and intercept, and plot the regression line against the observed data.

### 5. 🧩 Multiple Linear Regression

Train a model with multiple property features. Compare its evaluation metrics with the simple model to see whether using more information improves predictions.

### 6. 🌱 Polynomial Regression

Try polynomial features of degree 2 and degree 3 to model curved relationships. Compare the results and keep in mind that a more complex curve does not automatically mean a better model.

### 7. ⚙️ Gradient Descent

Implement three update approaches from scratch:

- **Batch Gradient Descent** — calculates each update using the full training set.
- **Stochastic Gradient Descent (SGD)** — updates parameters using one training example at a time.
- **Mini-Batch Gradient Descent** — updates parameters using a small group of training examples.

Compare the training behaviour, convergence plots, and time measurements produced by the notebook.

### 8. 🔎 Model Diagnostics and Final Review

Review prediction errors and compare training and test performance. Use these results to discuss model fit and select a model based on measured performance—not assumptions.

## 📈 Models and Evaluation

The notebook explores these methods:

| Model | Purpose |
|---|---|
| 📏 Simple Linear Regression | Estimate price from `area_sqft` alone |
| 🧩 Multiple Linear Regression | Use several features to estimate price |
| 🌱 Polynomial Regression (degree 2) | Test a curved relationship |
| 🌿 Polynomial Regression (degree 3) | Test a more flexible curve |
| ⚙️ Gradient Descent variants | Compare optimization approaches |

The best model should be identified **after running the notebook** and comparing its test-set results. This README does not claim a winning model or a particular accuracy score in advance.

## 📊 Metrics Explained

| Metric | What it tells us | Preferred direction |
|---|---|---|
| **MAE** — Mean Absolute Error | Average absolute difference between actual and predicted prices | Lower |
| **MSE** — Mean Squared Error | Average squared prediction error; larger errors receive more weight | Lower |
| **RMSE** — Root Mean Squared Error | Typical error scale, expressed in the target's units | Lower |
| **R²** — R-squared | How much variation in the target is explained by the model | Usually higher |
| **Adjusted R²** | R² adjusted for the number of input features | Useful for comparing models with different feature counts |

📌 **Tip:** Do not judge a model using just one metric. Review error values together with test-set performance and the diagnostic plots.

## 🚀 Getting Started

### ✅ Requirements

- Python 3.x
- Jupyter Notebook or JupyterLab
- The Excel dataset used by the notebook

### 1️⃣ Download the Project

Download or clone the repository to your computer. Keep the notebook and dataset in the same folder unless the file path in the notebook is changed.

### 2️⃣ Install the Required Libraries

Open a terminal in your project folder and run:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
```

### 3️⃣ Check the Files

Make sure the folder contains the notebook and dataset:

```text
House-Price-Prediction/
├── House_Price_Prediction_Short_No_Theory.ipynb
├── RealEstate_HousePrice_Dataset_4200.xlsx
└── README.md
```

If the notebook has been renamed, use its current filename instead.

### 4️⃣ Launch Jupyter

```bash
jupyter notebook
```

Open the notebook in your browser.

### 5️⃣ Run the Notebook

Run each cell from top to bottom. Check that the dataset loads successfully and review the generated plots, metric values, and model comparisons.

> 🧩 **Troubleshooting:** If Python cannot find the Excel file, check the notebook's working directory and make sure the dataset filename matches the one used in the code.

## 📁 Project Structure

```text
House-Price-Prediction/
│
├── 📓 House_Price_Prediction_Short_No_Theory.ipynb
│   └── Data analysis, regression models, evaluation, and plots
│
├── 📊 RealEstate_HousePrice_Dataset_4200.xlsx
│   └── Property features and house-price target
│
└── 📄 README.md
    └── Project overview and instructions
```

## 🔎 Key Questions Explored

This project is designed to explore questions such as:

- 📏 Does house area show a relationship with house price?
- 🧩 Does using several property features improve prediction?
- 🌱 Do polynomial features capture patterns that a straight line misses?
- ⚙️ How do Batch, Stochastic, and Mini-Batch Gradient Descent differ in their updates and convergence?
- 📉 How do training and testing errors compare?
- 🧠 Do the results suggest underfitting or overfitting?

The answers should come from the notebook's actual output after it has been run.

## 💡 Possible Improvements

Future versions of this project could include:

- 📦 A reusable preprocessing and modelling pipeline.
- 🔁 Cross-validation for a more stable model comparison.
- 🎛️ Hyperparameter tuning for polynomial models and gradient descent.
- 📉 Residual analysis and additional diagnostic plots.
- 🧪 A baseline model for comparison.
- 💾 Saving the fitted model for later predictions.
- 🖥️ A small web interface where users enter property details and receive an estimated price.
- 📋 A clearer comparison table containing verified test metrics for each model.

## ⚠️ Limitations

- This is an educational machine-learning project, not a professional property valuation service.
- Model performance depends on the quality and representativeness of the dataset.
- The dataset's location score and other fields may not capture every factor that affects real property prices.
- Evaluation scores should be calculated from the actual notebook run; they are not guaranteed in advance.
- Predictions should be treated as estimates, not as financial or real-estate advice.

## 👨‍💻 Author

**Created by:** `Your Name`

> Replace `Your Name` with your name or GitHub username before publishing the repository.

Connect with me on GitHub: [@your-github-username](https://github.com/your-github-username) *(replace with your GitHub username)*.

## 👤 Project Details

| Detail | Information |
|---|---|
| **Project name** | House Price Prediction |
| **Project theme** | Predictive Insight Engine — Supervised Learning |
| **Problem type** | Regression |
| **Target variable** | `house_price_inr` |
| **Language** | Python |
| **Environment** | Jupyter Notebook |
| **Purpose** | Practice data analysis, regression modelling, and model evaluation |

---

<div align="center">

### 🌟 Thanks for checking out this project!

**Explore the data · Train the models · Compare the results · Learn from the errors**

<sub>Made for learning and experimentation with supervised machine learning.</sub>

</div>
