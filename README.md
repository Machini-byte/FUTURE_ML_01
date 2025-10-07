# FUTURE_ML_01
Retail sales forecasting using prophet: A predictive model built using Facebook's prophet library to forecast retail sales. This project demonstrates my expertise in time series forecasting, data analysis, and machine learning. Feel free to explore the code, and let's collaborate!



#  Retail Sales Forecasting using Prophet

##  Project Overview
This project focuses on forecasting **retail sales** using historical data to help businesses plan inventory, marketing, and staffing.  
The model is built using **Facebook Prophet**, a powerful time series forecasting algorithm capable of capturing both **trend** and **seasonality** patterns.

---

##  Business Problem
Retail companies often face challenges in anticipating future sales due to market fluctuations and seasonality.  
Accurate forecasting helps:
- Prevent stockouts or overstocking  
- Optimize resource allocation  
- Improve revenue projections  

---

##  Objective
Develop a time series model that accurately predicts **daily retail sales** for the next **two years**, providing business insights on sales trends and seasonality.

---

##  Dataset Description
- **Source:** Mock Kaggle Retail Dataset (`mock_kaggle.csv`)
- **Variables:**
  - `Date` → Date of sales record  
  - `Sales` → Daily total sales
   

The data was cleaned, formatted, and transformed into Prophet’s required structure (`ds` for date and `y` for sales).

---

##  Data Preprocessing
- Converted date column to datetime format    
- Renamed columns to Prophet’s format (`ds`, `y`)
  

---

##  Exploratory Data Analysis (EDA)
- **Trend Analysis:** Sales show steady growth over time.  
- **Seasonality:**  
  - Sales drop during the **Fall season**  
  - Sales peak during **Spring** due to increased consumer demand  

---

##  Model Development
**Algorithm Used:** Facebook Prophet  

Prophet was selected because it:
- Handles trend and seasonality automatically  
- Can easily forecast long-term horizons  
- Is interpretable and suitable for business contexts  

**Forecast Duration:** 2 years (730 days)

---

## Model Evaluation

| Metric | Score |
|---------|-------|
| MAE | **56.38** |
| RMSE | **73.84** |
| SMAPE | **66.01%** |

###  Observations
- Sales tend to be **low during the Fall season**  
- Sales tend to be **high during the Spring season**  
- Despite the moderate SMAPE (66%), the model captures seasonality effectively.  
  Further tuning or inclusion of exogenous features (e.g., promotions, holidays) could improve accuracy.

---

##  Visualization Highlights
- **Actual vs Forecasted Sales Plot**  
  Shows predicted sales trend compared with real data.
  
- **Trend Line (Forecast vs Actuals)**  
  Highlights seasonal changes and overall growth pattern.

- **Forecast Components Plot**  
  Displays trend, weekly, and yearly seasonal effects detected by Prophet.

---

##  Business Insights
- Spring months show **the highest projected sales** — ideal for targeted promotions.  
- Fall shows **lower sales** — indicating a potential for discount campaigns.  
- Long-term forecasts suggest **steady overall growth**, meaning expanding product range or branch coverage could be strategic.

---

---

##  How to Run the Project
```bash
# 1. Clone the repository
git clone https://github.com/kevinmachini/retail-sales-forecasting.git
cd retail-sales-forecasting

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the notebook
jupyter notebook retail_sales_forecasting.ipynb
