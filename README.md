# 📊 Crime Data Analysis & Time Series Forecasting (2014–2019)

## 📌 Project Overview
This project performs **Exploratory Data Analysis (EDA)** and **Time Series Forecasting** on crime data from **2014 to 2019**.  
The goal is to analyze crime trends, visualize crime distributions, and forecast future crime counts using **SARIMA** and **Facebook Prophet** models.

---

## 📂 Dataset
- **File**: `MCI_2014_to_2019.csv`
- **Source**: Crime records dataset
- **Key Columns**:
  - `MCI` – Major Crime Indicator
  - `offence` – Type of offence
  - `reporteddate` – Date crime was reported
  - `occurrencedate` – Date crime occurred
  - `occurrenceyear`, `occurrencemonth`, `occurrenceday`

---

## 🛠️ Technologies & Libraries Used
- **Python 3.9+**
- **Data Handling**: pandas, numpy
- **Visualization**: matplotlib, seaborn
- **Statistical Modeling**: statsmodels
- **Machine Learning Metrics**: scikit-learn
- **Time Series Forecasting**:
  - SARIMA (statsmodels)
  - Facebook Prophet
- **Utilities**: tqdm, itertools, warnings

---

## 🔍 Exploratory Data Analysis (EDA)
The following analyses are performed:

### ✔ Crime Distribution
- Crime count by **Major Crime Indicator (MCI)**
- Offence-wise distribution for:
  - Assault
  - Auto Theft
  - Break and Enter
  - Robbery
  - Theft Over

### ✔ Time-Based Analysis
- Monthly crime trends
- Daily crime occurrences
- Reporting delay analysis

---

## ⏳ Time Series Analysis
### 1️⃣ Data Preparation
- Converted date columns to `datetime`
- Aggregated crime counts per day
- Resampled monthly data
- Seasonal decomposition (Trend, Seasonality, Residuals)

---

## 📈 Forecasting Models

### 🔹 SARIMA (Seasonal ARIMA)
- Grid search over `(p, d, q)` and seasonal parameters
- Best model selected using **AIC**
- Forecasted next **365 days**
- Performance metrics:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - Upper & Lower confidence bounds

### 🔹 Facebook Prophet
- Daily seasonality enabled
- Forecasted next **365 days**
- Compared Prophet predictions with SARIMA
- Error analysis using MSE and RMSE

---

## 📊 Model Comparison
- SARIMA vs Prophet forecasts
- Confidence interval comparison
- Visual comparison of predictions vs actual crime counts

---

## 🧠 Crime-Type Wise Forecasting
Separate **Prophet models** were trained for:
- **Assault**
- **Auto Theft**

Each includes:
- Forecast plots
- Confidence intervals
- Actual vs predicted comparison

---

## 📌 Results & Insights
- Clear **seasonal patterns** in crime data
- SARIMA performs well on structured seasonal data
- Prophet adapts better to trend changes
- Combined approach provides more reliable insights

---

## ▶️ How to Run the Project

### 1️⃣ Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn prophet tqdm ipykernel
2️⃣ Run the Project
Ensure the dataset MCI_2014_to_2019.csv is in the project directory.

bash
Copy code
python crime_forecasting.py
Or open the notebook in VS Code / Jupyter.

📌 Future Enhancements
LSTM-based forecasting

Hyperparameter tuning for Prophet

Crime-type clustering

Interactive dashboard using Streamlit

👤 Author
Ajay Reddy

GitHub: https://github.com/ajayreddy8691
LinkedIn: https://www.linkedin.com/in/ajayreddy8691/
LeetCode: https://leetcode.com/u/ajayreddy8691/
