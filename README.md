📊 Walmart Weekly Sales Forecasting
Business-Oriented Time Series Machine Learning Project
📌 Problem Statement

Accurate demand forecasting is critical for large retailers like Walmart to optimize inventory, staffing, and promotions. Poor forecasts result in overstocking or lost sales.

This project builds a time-aware machine learning model to predict weekly department-level sales using historical data, promotions, store attributes, and economic indicators.

🗂️ Dataset

Source: Walmart Store Sales Forecasting (Kaggle)

Datasets used:

train.csv – Historical weekly sales

features.csv – Promotions, fuel price, CPI, unemployment

stores.csv – Store size and type

test.csv – Future periods for prediction

⚙️ Approach

Merged multiple datasets into a unified analytical table

Engineered time-based features (Year, Month, Week)

Created lag and rolling demand features to capture seasonality

Used a time-based train–validation split to avoid data leakage

Trained a Random Forest Regressor for non-linear demand modeling

📈 Model Performance

Baseline MAE (Last Week Sales): $1,718

Random Forest MAE: $1,495

Improvement over baseline: 12.99%

Holiday MAE: $1,794
Non-Holiday MAE: $1,480

🔍 Key Insights

Recent sales history (lag_1, rolling_mean_4) is the strongest predictor of demand

Holiday weeks exhibit higher volatility and forecasting error

Promotional markdowns positively influence weekly sales

Macroeconomic factors have limited short-term impact at weekly granularity

🧠 Business Recommendations

Use rolling sales trends for short-term inventory planning

Allocate buffer stock for holiday weeks due to higher uncertainty

Optimize promotions by department rather than store-wide

Focus demand forecasting efforts at Store–Department level

🛠️ Tech Stack

Python (NumPy, Pandas, Matplotlib, Seaborn)

Scikit-learn

Jupyter Notebook