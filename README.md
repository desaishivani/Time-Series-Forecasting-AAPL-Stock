# 📈 Financial Time Series Forecasting: AAPL Stock

This project compares traditional ARIMA and deep learning (LSTM) models to forecast Apple Inc. (AAPL) stock prices over time using historical data from Yahoo Finance.

---

## 📊 Dataset
- Source: Yahoo Finance (`yfinance`)
- Range: Jan 2018 – Dec 2023
- Fields used: `Date`, `Close`, `Volume`

---

## 🔍 Project Objectives
- Clean and prepare time series data
- Test stationarity and apply transformations
- Build ARIMA model and evaluate performance
- Build and train LSTM model for non-linear forecasting
- Compare performance of classical and deep learning methods

---

## 🧠 Methods

### ARIMA
- ADF test for stationarity
- Auto ARIMA (AIC optimization)
- Forecasted 30 business days
- RMSE: ~11.88, MAE: ~9.35

### LSTM
- Sequence windowing (60-day input)
- Model architecture: 2 LSTM layers + Dense
- Forecasted next 30 days
- Captured short-term trend shifts better than ARIMA

---

## 📈 Visualizations

- Actual vs Forecast (ARIMA)
- Actual vs Forecast (LSTM)
- 30-day future forecast plots

---

## 💡 Key Takeaways
- ARIMA performed best on stable, trend-driven periods.
- LSTM better captured directional shifts in recent data.
- Combining both methods improves understanding of forecast scenarios.

---

## 🛠️ Tools Used
- Python, Pandas, Matplotlib
- Statsmodels (ARIMA), pmdarima (auto_arima)
- TensorFlow / Keras (LSTM)
- scikit-learn (MinMaxScaler, metrics)

---

## 📂 Structure
- `notebooks/forecast_arima_vs_lstm.ipynb`
- `data/aapl_stock.csv`
- `models/lstm_model.h5`
- `README.md`

---

## 🔮 Future Improvements
- Include external features (macro trends, sentiment)
- Use rolling evaluation / walk-forward validation
- Extend to multivariate LSTM or transformer models

