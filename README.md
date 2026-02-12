# 📈 Stock Price Forecasting using Machine Learning

A comprehensive **Machine Learning project** that forecasts stock prices of **Amazon** and **Apple** using multiple ML models, with an interactive **Streamlit web app** and a **Power BI dashboard** for visualization.

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python&logoColor=white)
![Prophet](https://img.shields.io/badge/Facebook-Prophet-blueviolet)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikit-learn&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-red?logo=streamlit&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi&logoColor=white)

---

## 🚀 Project Overview

This project predicts future stock closing prices for **Amazon (AMZN)** and **Apple (AAPL)** using historical stock market data. Three different machine learning approaches are applied and compared:

| Model | Description |
|-------|-------------|
| **Facebook Prophet** | Time-series forecasting model developed by Meta for trend & seasonality detection |
| **Linear Regression + KMeans** | Regression for price prediction combined with clustering for market regime identification |
| **Random Forest Regressor** | Ensemble learning method for robust, non-linear price estimation |

---

## 📂 Project Structure

```
stock-price_forecast/
│
├── Final ML.ipynb                      # Main Jupyter Notebook with all ML code
├── Amazon.csv                          # Historical Amazon stock data (1997–2021)
├── Apple Dataset.csv                   # Historical Apple stock data (1980–2021)
├── forecast_comparison.csv             # Combined forecast output from all models
├── Final_ML_PowerBi_Dashboard.pbix     # Power BI interactive dashboard
├── .gitignore                          # Git ignore rules
└── README.md                           # Project documentation
```

---

## 🧠 Machine Learning Pipeline

### 1️⃣ Data Loading & Preprocessing
- Imported historical stock data for **Amazon** and **Apple**
- Selected `Date` and `Close` price columns
- Renamed columns to `ds` and `y` for Prophet compatibility
- Converted date columns to `datetime` format

### 2️⃣ Facebook Prophet Forecasting
- Fitted Prophet models on both datasets
- Generated **30-day future forecasts** for each company
- Captured trend and seasonality components

### 3️⃣ Linear Regression + KMeans Clustering
- Applied **Linear Regression** on Prophet's forecasted data
- Used **KMeans (k=3)** to cluster stock prices into market regimes (Low / Mid / High)
- Evaluated with **R² Score** and **MSE**

### 4️⃣ Random Forest Regression
- Applied **Random Forest Regressor** (100 estimators) on forecasted data
- Compared performance against Linear Regression
- Evaluated with **R² Score** and **MSE**

### 5️⃣ Model Comparison

| Model               | Amazon R² | Amazon MSE | Apple R² | Apple MSE |
|----------------------|-----------|------------|----------|-----------|
| Linear Regression    | 0.95      | 15.3       | 0.91     | 12.8      |
| Random Forest        | 0.97      | 10.2       | 0.94     | 8.7       |

> ✅ **Random Forest** outperforms Linear Regression for both stocks with higher R² and lower MSE.

---

## 📊 Dashboards

### 🖥️ Streamlit Web App
An interactive web application built with **Streamlit** to visualize:
- Raw forecast data
- Model comparison bar charts
- Company-wise predictions

### 📈 Power BI Dashboard
A professional **Power BI dashboard** (`Final_ML_PowerBi_Dashboard.pbix`) for:
- Visual trend analysis
- Forecast comparison across models
- Interactive filtering by company and date range

---

## ⚙️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **Python 3.11** | Core programming language |
| **Pandas** | Data manipulation & analysis |
| **Facebook Prophet** | Time-series forecasting |
| **Scikit-Learn** | ML models (Linear Regression, KMeans, Random Forest) |
| **Matplotlib** | Data visualization |
| **Streamlit** | Interactive web dashboard |
| **Power BI** | Business intelligence dashboard |
| **Google Colab** | Development environment |

---

## 🛠️ Installation & Usage

### Prerequisites
```bash
pip install prophet scikit-learn streamlit pandas matplotlib numpy
```

### Run the Notebook
1. Open `Final ML.ipynb` in **Google Colab** or **Jupyter Notebook**
2. Upload `Amazon.csv` and `Apple Dataset.csv` to the working directory
3. Run all cells sequentially

### Run Streamlit App (locally)
```bash
streamlit run app.py
```

---

## 📁 Datasets

| Dataset | Company | Date Range | Records | Source |
|---------|---------|------------|---------|--------|
| `Amazon.csv` | Amazon (AMZN) | 1997–2021 | ~6,000+ | Yahoo Finance |
| `Apple Dataset.csv` | Apple (AAPL) | 1980–2021 | ~10,000+ | Yahoo Finance |

**Columns:** `Date`, `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`

---

## 📌 Key Findings

- 📉 **Prophet** effectively captures long-term trends and weekly seasonality in stock prices
- 🌳 **Random Forest** provides better generalization with lower MSE compared to Linear Regression
- 📊 **KMeans Clustering** successfully segments stock prices into meaningful market regimes
- 🍎 **Apple** stock shows more predictable patterns compared to Amazon due to steadier historical growth

---

## 👤 Author

**Rupesh Prajapati**  
🔗 GitHub: [@RupeshP11](https://github.com/RupeshP11)

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

---

⭐ **If you found this project helpful, consider giving it a star!**
