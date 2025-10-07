# Stock Forecast AI 📈

AI-powered stock analysis tool that predicts short-term price movements using trends, candlestick patterns, and news sentiment.

## 🚀 Overview

Stock Forecast AI combines price action and NLP-based sentiment signals to forecast stock trends.  
It provides:

- Machine learning models (LightGBM, LSTM, Transformers)
- Candlestick & technical pattern recognition
- FinBERT-based news sentiment analysis
- Interactive Streamlit dashboard for visualization
- Walk-forward backtesting and explainability with SHAP

⚠️ **Disclaimer:** This project is for research and educational purposes only — **not financial advice**.

---

## 🧩 Features

- Daily price ingestion from `yfinance`, `finnhub`, and `newsapi`
- 50+ technical indicators and candlestick pattern detection
- FinBERT sentiment scoring for financial news
- Rolling retraining and walk-forward validation
- Backtesting with Sharpe ratio, drawdown, and hit-rate metrics
- Streamlit dashboard with predictions and explanations

---

## 🗂️ Structure
```bash
src/
├── ingest/ # Data fetching and updates
├── features/ # Indicator & pattern engineering
├── models/ # ML model training & forecasting
├── backtest/ # Strategy evaluation
├── api/ # REST API via FastAPI
└── app/ # Streamlit dashboard
```

---

## ⚙️ Setup

### 1. Clone the repo

```bash
git clone https://github.com/KinTatHo/stock-forecast-ai.git
cd stock-forecast-ai
```

### 2. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate    # macOS/Linux
venv\Scripts\activate       # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Copy the example file and insert your API keys:

```bash
cp .env.example
```

Example .env:

```bash
FINNHUB_API_KEY=your_key
NEWSAPI_KEY=your_key
ALPHA_VANTAGE_KEY=your_key
POLYGON_API_KEY=
DATA_PATH=./data
MODEL_PATH=./models
```

Free keys can be obtained from:

[Finnhub.io](https://finnhub.io)

[NewsAPI.org](https://newsapi.org/)

[AlphaVantage.co](https://www.alphavantage.co/)
