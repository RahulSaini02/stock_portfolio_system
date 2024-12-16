# Stock Portfolio Prediction Model

## Abstract

This project develops a **Portfolio Prediction Model** to forecast stock prices and provide actionable insights for portfolio management. Leveraging **Long Short-Term Memory (LSTM)** networks, the model captures sequential dependencies in stock market data. The focus is on a portfolio comprising **AAPL, TSLA, and GOOGL**. Key steps include data preprocessing, feature engineering, model training, and profit/loss evaluation. The findings demonstrate the model's ability to deliver accurate predictions, aiding investors in decision-making.

---

## Concepts and Keywords

**Concepts:**

- Data Collection and Preprocessing
- Feature Engineering
- Time-Series Analysis
- LSTM Networks
- Sliding Window Approach
- Model Training and Evaluation
- Data Normalization and Visualization

**Keywords:**
Portfolio Management, Profit/Loss Analysis, Sequential Dependencies, Sliding Window Approach, Financial Forecasting, AAPL, TSLA, GOOGL.

---

## Introduction

Financial markets are highly volatile, making stock price prediction essential for portfolio optimization. This project integrates data mining, machine learning, and visualization techniques to forecast stock trends and evaluate portfolio performance.

### Objectives

1. Predict next-day stock prices using historical data.
2. Evaluate portfolio performance with profit/loss metrics.

---

## Data Collection and Preparation

**Data Source:**

- Historical stock data retrieved using the `yfinance` library.

**Preprocessing Steps:**

1. **Handling Missing Data**: Forward-fill method.
2. **Outlier Removal**: Excluded rows with non-positive `Close` values.
3. **Feature Selection**: Focused on `Close` due to strong correlations.
4. **Temporal Transformation**: Sliding window approach (60-day lookback).

---

## Prediction Models

### 1. Random Forest Regressor

- Ensemble learning method for non-linear trends.
- Metrics:
  - **MAE**: 18.22
  - **MSE**: 735.97
  - **RMSE**: 27.12

### 2. Long Short-Term Memory (LSTM)

- Sequential model for time-series data.
- Metrics:
  - **MAE**: 5.07
  - **MSE**: 39.14
  - **RMSE**: 6.30

**Result:** LSTM outperformed Random Forest due to its ability to capture sequential dependencies.

---

## Portfolio Prediction System

The system automates stock prediction workflows using custom classes:

1. **StockPredictionModel**: Handles LSTM design, training, and evaluation.
2. **Stock**: Automates data fetching and preparation.
3. **PortfolioPredictor**: Manages multi-stock portfolios, profit/loss calculations, and next-day predictions.

---

## Results

### Model Performance

- **LSTM**: Accurate predictions with better adaptation to volatility.
- **Random Forest**: Less effective for sequential data.

### Portfolio Insights

- **Profit/Loss Estimation**: Based on price predictions and portfolio weights.
- **Visualization**: Comparative plots of actual vs. predicted prices.

---

## Discussion and Future Work

**Key Takeaways:**

- LSTM models excel in capturing sequential dependencies.
- High market volatility poses challenges for all models.

**Future Directions:**

- Explore **Transformers** and hybrid models for improved accuracy.
- Develop a real-time portfolio dashboard for tracking and decision-making.

---

## References

1. GeeksforGeeks: [Introduction to LSTM](https://www.geeksforgeeks.org/deep-learning-introduction-to-long-short-term-memory/)
2. Keras: [Sequential Model](https://keras.io/guides/sequential_model/)
3. Medium: [Yahoo Finance with yfinance](https://medium.com/@euricopaes/extracting-data-from-yahoo-finance-with-yfinance-96798253d8ca)
4. YouTube: [Stock Price Prediction](https://youtu.be/QIUxPv5PJOY?si=PKt44abYBiXmbjg1)

This markdown version retains the structure and content of the PDF while being formatted for markdown compatibility. Let me know if you’d like further adjustments!
`