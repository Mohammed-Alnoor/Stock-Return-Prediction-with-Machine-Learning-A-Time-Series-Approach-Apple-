#  Stock Price Prediction using Machine Learning

## Overview

This project focuses on predicting short-term stock returns using machine learning models. The goal is not just to build models, but to understand how difficult financial prediction is and where real improvements come from.

---

##  Dataset

The dataset contains historical stock data including:

* Open, High, Low, Close prices
* Volume
* Time-based records

From this data, additional features were engineered to improve model performance.

---

##  Exploratory Data Analysis (EDA)

Key observations:

* Stock returns are highly noisy
* Weak correlation between features and target
* No strong linear relationships
* High volatility across time

These findings explain why prediction is challenging.

---

##  Feature Engineering

The following features were created:

* Lag features (previous prices/returns)
* Rolling statistics (mean, std)
* Volatility measures
* Momentum indicators

Feature engineering provided small but consistent improvements.

---

##  Modeling

### Models used:

* Linear Regression (Baseline)
* LightGBM (Final Model)

### Validation:

* TimeSeriesSplit (to respect time order)

---

##  Results

| Model             | MAE    | RMSE   |
| ----------------- | ------ | ------ |
| Linear Regression | ~0.025 | ~0.035 |
| LightGBM          | ~0.020 | ~0.028 |

👉 LightGBM outperformed the baseline, but improvements were limited.

---

##  Visualizations

The project includes:

* Actual vs Predicted values
* Residual distribution
* Feature importance
* Prediction vs Actual scatter

These help evaluate model behavior beyond metrics.

---

##  Key Insights

* Predicting exact stock returns is inherently difficult
* Market data contains a high level of noise
* Non-linear models perform better than linear ones
* Feature engineering has more impact than model complexity
* Model performance is unstable across time

---

##  Limitations

* Weak signal in short-term returns
* No external data (news, sentiment, macro factors)
* Models are sensitive to market conditions
* Results may not generalize across different stocks

---

##  Future Work

* Try classification (predict up/down instead of exact value)
* Add sentiment or news data
* Explore deep learning models (LSTM, Transformers)
* Build trading strategy on top of predictions

---

##  Tech Stack

* Python
* Pandas, NumPy
* Matplotlib
* Scikit-learn
* LightGBM

---

##  Conclusion

This project shows that improving prediction accuracy in financial markets is less about choosing complex models and more about understanding the data and designing meaningful features.

---

##  Project Structure

```
stock-price-prediction/
│
├── data/
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_feature_engineering.ipynb
│   └── 05_modeling.ipynb
│
├── README.md
└── requirements.txt
```
