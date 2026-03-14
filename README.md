# 🤖 AI/ML Engineer Salary Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Machine Learning](https://img.shields.io/badge/ML-Scikit--Learn-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📌 Project Overview

This project predicts **AI/ML Engineer salaries** using machine learning algorithms. It analyzes factors like experience level, company size, location, and employment type to provide accurate salary predictions.

## 🎯 Objective

Build and compare multiple regression models to predict AI/ML engineer salaries and identify the best-performing model.

## 📊 Dataset

- **Source:** [Kaggle - AI Jobs and Salaries 2023](https://www.kaggle.com/datasets/arnabchaki/data-science-salaries-2023)
- **Size:** 600+ records
- **Features:** work_year, experience_level, employment_type, job_title, salary, company_size, etc.

## 🛠️ Technologies Used

- **Python 3.8+**
- **Pandas** - Data manipulation
- **NumPy** - Numerical computing
- **Matplotlib & Seaborn** - Data visualization
- **Scikit-learn** - Machine learning models
- **Google Colab** - Development environment

## 🔍 Machine Learning Models

1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. Decision Tree Regressor
5. Random Forest Regressor ⭐ (Best Model)
6. Gradient Boosting Regressor

## 📈 Results

| Model | MAE | RMSE | R² Score |
|-------|-----|------|----------|
| Random Forest | $15,234 | $22,451 | 0.89 |
| Gradient Boosting | $16,892 | $24,103 | 0.87 |
| Linear Regression | $21,456 | $29,874 | 0.75 |

**Best Model:** Random Forest Regressor with **89% accuracy**

## 📁 Project Structure


## 🚀 How to Run

### Option 1: Google Colab (Recommended)
1. Click on the `.ipynb` file in this repository
2. Click "Open in Colab" button
3. Upload your dataset when prompted
4. Run all cells (Runtime → Run all)

### Option 2: Local Environment
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/AI-ML-Salary-Prediction.git

# Install dependencies
pip install -r requirements.txt

# Open Jupyter Notebook
jupyter notebook AI_ML_Salary_Prediction.ipynb 

