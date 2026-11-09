# 🤖 AI/ML Engineer Salary Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Machine Learning](https://img.shields.io/badge/ML-Scikit--Learn-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📌 Project Overview

This project predicts **AI/ML Engineer salaries** using machine learning algorithms. It analyzes factors like experience level, company size, location, and employment type to provide accurate salary predictions.

## 🎯 Objective

Build and compare multiple regression models to predict AI/ML engineer salaries and identify the best-performing model.

## 📊 Dataset

- **Source:** [Glassdoor Jobs Dataset (Kaggle)](https://www.kaggle.com/datasets/promptcloud/jobs-on-naukricom) — scraped Glassdoor job postings
- **Raw size:** 956 job listings, 15 columns
- **Usable after cleaning:** 704 listings (invalid salary placeholders and hourly wages removed)
- **Columns:** Job Title, Salary Estimate, Rating, Company Name, Location, Size, Founded, Type of ownership, Industry, Sector, Revenue, Competitors, Job Description

## 🛠️ Technologies Used

- **Python 3.8+**
- **Pandas** - Data manipulation
- **NumPy** - Numerical computing
- **Matplotlib, Seaborn & Plotly** - Data visualization
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

All six models were trained on the same 80/20 split (563 train / 141 test samples):

| Model | MAE | RMSE | R² Score |
|-------|-----|------|----------|
| **Random Forest** ⭐ | **$12,988** | **$20,227** | **0.70** |
| Gradient Boosting | $16,601 | $22,493 | 0.63 |
| Decision Tree | $10,991 | $23,914 | 0.59 |
| Ridge Regression | $24,574 | $30,732 | 0.32 |
| Lasso Regression | $24,766 | $30,983 | 0.31 |
| Linear Regression | $24,770 | $30,990 | 0.31 |

**Best Model:** Random Forest Regressor

- **R² of 0.70** → the model explains ~70% of the variation in salaries
- **MAE of ~$13K** → on average, predictions miss the actual salary by about $13,000
- Decision Tree has a slightly lower MAE but much worse RMSE and R² — it makes occasional huge misses, while Random Forest is the most stable overall

### 🔑 Feature Importance (Random Forest)

| Feature | Importance |
|---------|-----------|
| Job role (simplified) | 26.6% |
| Job state | 11.5% |
| Seniority level | 11.2% |
| Company age | 8.5% |
| Company rating | 7.6% |

## 📁 Project Structure

```text
AI-ML-Salary-Prediction/
├── salpred.ipynb                        # Full notebook (EDA → cleaning → training → evaluation)
├── glassdoor_jobs.csv                   # Raw dataset (956 Glassdoor job listings)
├── best_salary_prediction_model.pkl     # Saved Random Forest model (pickle)
└── README.md
```

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
1. Click on the `salpred.ipynb` file in this repository
2. Click "Open in Colab" button
3. Upload your dataset when prompted
4. Run all cells (Runtime → Run all)

### Option 2: Local Environment
```bash
# Clone the repository
git clone https://github.com/binarybyte23/AI-ML-Salary-Prediction.git
cd AI-ML-Salary-Prediction

# Install dependencies
pip install pandas numpy matplotlib seaborn plotly scikit-learn

# Open Jupyter Notebook
jupyter notebook salpred.ipynb
```

