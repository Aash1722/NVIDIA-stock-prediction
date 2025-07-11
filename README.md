
# NVIDIA Stock Price Prediction using Machine Learning

This project explores the use of machine learning and deep learning models to forecast NVIDIA stock prices, using methods that approximate stochastic behaviors like Brownian motion. It combines insights from mathematical finance and time-series modeling to build interpretable and effective forecasting tools.

## 📊 Project Overview

Traditional stock price models like Geometric Brownian Motion (GBM) often fail to capture the non-linear, noisy, and path-dependent behavior of real-world financial markets. This project aims to learn such dynamics from historical NVIDIA stock data (2015–2024) using:

- **Random Forest Regressor**
- **LSTM Neural Network**
- **Hybrid LSTM + AdaBoost Ensemble**

These models are evaluated for their ability to approximate **drift** and **volatility** patterns, offering data-driven alternatives to classical SDE-based approaches.

---

## 🧠 Methodology

### 📌 Feature Engineering
Derived a variety of technical indicators to emulate Brownian path statistics:

- **Trend Features:** SMA, EMA
- **Momentum Indicators:** MACD, RSI
- **Volatility Measures:** ATR, TR
- **Volume Metrics:** OBV, VWAP
- **Temporal Indicators:** Daily Return, RoC, Day/Month/Year

### 🤖 Models Used

- **Random Forest Regressor:** Used for baseline modeling and feature importance.
- **LSTM (Long Short-Term Memory):** Captures sequential dependencies in stock prices.
- **LSTM + AdaBoost:** Hybrid approach combining temporal learning with ensemble correction.

---

## 📈 Results

| Model              | Test R² | Observations                              |
|-------------------|---------|-------------------------------------------|
| Random Forest      | 0.0977  | Good training fit, poor generalization     |
| LSTM               | 0.9360  | Best performance on test data              |
| LSTM + AdaBoost    | -1.8442 | Severe overfitting, low generalization     |

---

## 🔬 Discussion

- **Strengths of ML Models:**
  - Learn state-dependent drift and volatility.
  - Capture non-linear relationships and regime shifts.

- **Limitations:**
  - Lack of theoretical constraints like no-arbitrage.
  - Vulnerability to overfitting and noisy signals.

---

## 🔭 Future Work

- Calibrate LSTM paths with simulated GBM paths.
- Integrate stochastic volatility models (e.g., Heston).
- Connect with functional analysis tools (e.g., Karhunen–Loève expansion).

---

## 📚 References

- Karatzas & Shreve – *Brownian Motion and Stochastic Calculus*
- Breiman – *Random Forests*
- Hochreiter & Schmidhuber – *LSTM Networks*
- Bobrowski – *Functional Analysis for Probability and Stochastic Processes*
