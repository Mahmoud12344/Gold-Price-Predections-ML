# 📈 Gold Price Prediction — ML Comparative Study

> *Analyzing 2,290 days of financial market data to predict next-day gold prices using three regression models — benchmarked head-to-head across R², RMSE, and MAE.*

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

---

## 📌 Overview

This project explores whether next-day gold prices can be predicted from correlated financial market indicators. Using a dataset of **2,290 trading days** spanning **2008–2018**, it covers the full ML pipeline — data cleaning, EDA, feature engineering, model training, and visual benchmarking of three regression approaches.

---

## 📊 Dataset

| Feature | Description |
|---------|-------------|
| `GLD` | Gold ETF price (target) |
| `SPX` | S&P 500 index |
| `USO` | Oil ETF price |
| `SLV` | Silver ETF price |
| `EUR/USD` | Euro to US Dollar exchange rate |

- **2,290 rows**, no missing values, no duplicates
- Date column split into `Year`, `Month`, `DayOfWeek` features
- Target engineered as `Target_Next_Day_GLD` — tomorrow's gold price shifted into today's row

---

## 🔍 EDA Highlights

- **Silver (SLV)** has the strongest correlation with gold: **r = 0.87**
- **Oil (USO)** is negatively correlated: **r = −0.19**
- Gold price peaked around **2011–2012** then declined before recovering
- No outliers removed — boxplot inspection showed expected market variance

---

## 🤖 Models Compared

| Model | R² Score | RMSE | MAE |
|-------|----------|------|-----|
| Linear Regression | 0.8922 | 7.58 | 5.32 |
| Gradient Boosting | 0.9829 | 3.02 | 2.03 |
| **Random Forest** | **0.9882** | **2.51** | **1.62** |

**Random Forest** achieved the best performance across all three metrics.

---

## ⚙️ Pipeline

```
1. Load & inspect data        # shape, dtypes, nulls, duplicates
2. Feature engineering        # parse date → Year, Month, DayOfWeek
3. EDA & visualization        # heatmap, histplot, boxplot, scatterplot, lineplot
4. Target creation            # shift GLD by -1 to get next-day price
5. Train/test split           # 80/20
6. Train 3 models             # Linear Regression, Random Forest, Gradient Boosting
7. Evaluate & compare         # R², RMSE, MAE — table + bar charts
```

---

## 🛠️ Tech Stack

| | |
|-|-|
| Language | Python 3 |
| Data | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Modeling | Scikit-learn |
| Notebook | Jupyter |

---

## 🚀 Running Locally

```zsh
git clone https://github.com/<your-username>/gold-price-prediction.git
cd gold-price-prediction
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook gold_price_predections3.ipynb
```

**Requirements:**
```
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

---

## 📜 License

Fourth Semester Machine Learning Project — 2026.

---

<p align="center">Gold Price Prediction · ML Coursework · 2026</p>

 