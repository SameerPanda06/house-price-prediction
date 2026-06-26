# 🏠 House Price Predictor

A machine learning project that predicts house sale prices using Linear Regression, Ridge, and Lasso regression models built on the Kaggle House Prices dataset.

## 📁 Project Structure
house_price_project/
├── Data/
│   └── train.csv
├── models/
│   ├── linear_regression.pkl
│   ├── ridge.pkl
│   └── lasso.pkl
├── plots/
│   └── correlation_heatmap.png
├── train.py
├── app.py
└── README.md

## 🛠️ Tech Stack
- Python 3.x
- scikit-learn
- pandas, numpy
- matplotlib, seaborn
- joblib
- Streamlit

## ⚙️ Setup & Installation

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib streamlit
```

## 📊 Dataset
**Kaggle House Prices: Advanced Regression Techniques**  
https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data

Features used:
| Feature | Description |
|---|---|
| GrLivArea | Above grade living area (sq ft) |
| BedroomAbvGr | Number of bedrooms |
| FullBath | Number of bathrooms |
| YearBuilt | Year house was built |
| GarageCars | Garage capacity (cars) |
| OverallQual | Overall material and finish quality (1–10) |

Target: `SalePrice`

## 🚀 Run

```bash
# Step 1 — Train models
python train.py

# Step 2 — Launch dashboard
streamlit run app.py
```

## 🤖 Models

| Model | Description |
|---|---|
| Linear Regression | Baseline — interpretable coefficients |
| Ridge Regression | L2 regularization — handles multicollinearity |
| Lasso Regression | L1 regularization — automatic feature selection |

All models use `StandardScaler` inside a `sklearn Pipeline` to prevent data leakage.

## 📈 Results

| Model | R² | MAE | RMSE |
|---|---|---|---|
| Linear Regression | 0.9816 | ~$12,458 | ~$15,908 |
| Ridge Regression | 0.9816 | ~$12,460 | ~$15,908 |
| Lasso Regression | 0.9816 | ~$12,470 | ~$15,916 |

> Results may vary slightly with the real Kaggle dataset.

## 🖥️ Dashboard Features
- Predict house price by adjusting sliders
- Compare predictions across all 3 models
- Ensemble average of all model outputs
- Correlation heatmap of features

## 📚 Concepts Covered
- Supervised learning — regression
- Train/test split & cross-validation
- Feature scaling with StandardScaler
- L1 vs L2 regularization
- Model persistence with joblib
- Streamlit deployment
