# 📈 Gold Price Prediction — Linear Regression

A supervised machine learning project that builds a **Linear Regression model** to predict gold prices (GLD) using financial market indicators, with full correlation analysis, model evaluation, and residual diagnostics.

---

## 📌 Project Overview

This project uses historical gold price data (2008–2015) to predict the **GLD ETF closing price** from four correlated financial features: S&P 500 index, crude oil ETF, silver ETF, and EUR/USD exchange rate. The project covers the full regression pipeline from EDA to model interpretation.

---

## 🎯 Key Questions Answered

- What is the R² score and how well does the model fit the data?
- Does the residual plot reveal any patterns (non-linearity, heteroscedasticity)?
- Which feature has the strongest correlation with gold price?

---

## 📊 Results

| Metric | Value |
|--------|-------|
| **R² Score** | **0.8976** |
| MSE | — (see notebook) |
| RMSE | — (see notebook) |
| Strongest correlated feature | **SLV (Silver ETF)** |

**Interpretation:**
- The model explains **~89.76%** of the variance in gold prices — a strong fit for a linear model
- The residual plot reveals **heteroscedasticity**: errors are small at lower predicted prices but spread significantly at higher prices, suggesting the model becomes less precise in high-price regimes
- **Silver (SLV)** has the strongest positive correlation with gold — both are precious metals driven by similar macroeconomic forces

---

## 🗃️ Dataset

- **Name:** Gold Price Data (2008–2015)
- **Source:** [Kaggle — Gold Price Data](https://www.kaggle.com/datasets/altruistdelhite04/gold-price-data)
- **Rows:** 2,290 trading days
- **Date Range:** January 2008 – September 2015

| Column | Description |
|--------|-------------|
| `GLD` | Gold ETF price (target variable) |
| `SPX` | S&P 500 index |
| `USO` | Crude oil ETF |
| `SLV` | Silver ETF |
| `EUR/USD` | Euro to US Dollar exchange rate |

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3.x | Core language |
| Pandas | Data loading and cleaning |
| NumPy | Numerical operations |
| Scikit-learn | `LinearRegression`, `train_test_split`, metrics |
| Matplotlib & Seaborn | Correlation heatmap, residual plot, actual vs predicted |
| Jupyter Notebook | Interactive environment |

---

## 📁 Repository Structure

```
gold-price-linear-regression/
│
├── gold_price.ipynb           # Full regression pipeline notebook
├── gold_price_data.csv     # Dataset (2008–2015)
└── README.md               # Project documentation
```

---

## 🚀 How to Run

**1. Clone the repository**
```bash
git clone https://github.com/AmaanJilani1/gold-price-linear-regression.git
cd gold-price-linear-regression
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

**3. Launch the notebook**
```bash
jupyter notebook gold_price.ipynb
```

---

## 🔄 Pipeline Summary

```
gold_price_data.csv
      ↓
Drop null rows
      ↓
Feature selection: SPX, USO, SLV, EUR/USD → target: GLD
      ↓
Correlation heatmap (identify strongest predictors)
      ↓
Train/Test split (80/20, random_state=42)
      ↓
LinearRegression().fit()
      ↓
R² · MSE · RMSE · Residual Plot · Actual vs Predicted
```

---

## 📉 Visualizations

- **Correlation Heatmap** — shows pairwise relationships between all features and GLD
- **Residual Plot** — predicted values vs residuals to diagnose model fit
- **Actual vs Predicted** — line chart comparing true and predicted GLD prices across 50 test samples

---

## 💡 Key Insights

- Silver and gold are tightly coupled commodities — SLV is the single most predictive feature
- Heteroscedasticity in the residuals suggests a **polynomial or log-transformed model** could improve accuracy at higher price ranges
- EUR/USD and SPX have weaker but still meaningful correlations with gold, reflecting gold's role as a USD hedge

---

## 👤 Author

**Amaan Jilani**  
[GitHub](https://github.com/AmaanJilani1) · [LinkedIn](https://www.linkedin.com/in/amaanjilani/)

---
