# 🚗 Mercedes Stock Price Prediction using Machine Learning

## 📌 Project Overview

This project focuses on analyzing and predicting Mercedes-Benz stock prices using multiple machine learning models and a neural network.

The workflow includes exploratory data analysis (EDA), feature engineering, data preprocessing, and model evaluation.

---

## 📊 Dataset

* Historical stock price data (1996–2026)
* Features:

  * Open, High, Low, Close
  * Adjusted Close
  * Volume
  * Date (used to extract temporal features)

---

## 🔍 Exploratory Data Analysis (EDA)

* Visualization of stock price trends over time
* Distribution analysis of closing prices and returns
* Correlation analysis between variables
* Volatility and trading volume exploration

---

## ⚙️ Feature Engineering

New features were created to better capture market behavior:

* 📅 Time-based features: Year, Month, Day
* 📈 Daily Return (percentage change)
* ⚡ Volatility (High - Low)
* 📉 Moving Averages (MA50, MA200)

These features help models learn trends, seasonality, and price dynamics.

---

## 🧹 Data Preprocessing

* Handling missing values
* Train / Validation / Test split
* Feature scaling using StandardScaler

---

## 🤖 Models Used

* Linear Regression
* Random Forest Regressor
* HistGradientBoosting Regressor
* Neural Network (TensorFlow / Keras)

---

## 📈 Results

| Model             | MAE      | RMSE     | R² Score |
| ----------------- | -------- | -------- | -------- |
| Linear Regression | 0.239197 | 0.344102 | 0.999453 |
| Random Forest     | 0.241520 | 0.338408 | 0.999471 |
| Gradient Boosting | 0.243361 | 0.350469 | 0.999432 |
| Neural Network    | 0.448998 | 0.565622 | 0.998521 |

---

## 🔎 Key Insights

* All machine learning models achieved very similar performance
* Strong relationships exist between features and the target variable
* Tree-based models and linear models performed comparably well
* Neural networks were less effective for this tabular dataset

---

## ⚠️ Limitations

* Extremely high R² scores (~0.999) suggest potential data leakage
* Some engineered features (e.g., moving averages, returns) are derived from the target variable
* Random train-test split is not ideal for time-series data

---

## 🔮 Future Improvements

* Use time-based splitting instead of random splitting
* Replace current features with lag-based features to avoid data leakage
* Explore time-series models (LSTM, ARIMA)
* Incorporate external financial indicators

---

## 🛠️ Tools & Libraries

* Python
* Pandas, NumPy
* Scikit-learn
* TensorFlow / Keras
* Matplotlib, Seaborn

---

## 📁 Project Structure

```
📁 mercedes-stock-ml-analysis
│
├── data/
│   └── mercedes_stock.xlsx
├── comparing-ml-models-on-mercedes-stock-data.ipynb
├── README.md
├── requirements.txt
```

---

## 👤 Author

WENYAKE DIAMO ABOU

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```
