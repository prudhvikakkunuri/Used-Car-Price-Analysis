# 🚗 Used Car Price Analysis & Prediction

## 📌 Project Overview

The Indian used-car market is rapidly growing, but buyers often face **ambiguity and lack of transparency** while evaluating vehicle prices, mileage impact, fuel preferences, and resale value.  
This project focuses on **data-driven analysis of used car listings** to help users make **informed and confident purchasing decisions**.

The dataset was collected by **web scraping the Spinny used-car marketplace** using **BeautifulSoup and Selenium**.  
By applying **data cleaning, exploratory data analysis (EDA), hypothesis testing, and machine learning**, this project identifies key factors influencing used-car prices and predicts fair market value.

---

## 🎯 Business Problem

- Buyers struggle to assess whether a used car is **fairly priced or overpriced**
- Similar cars often show **large price variations**
- Lack of clarity on how **year, mileage, fuel type, transmission, brand, and location** affect price
- Decisions are often driven by **intuition rather than data**

### 💡 Objective
To **enhance decision-making for users planning to buy a used car** by:
- Removing ambiguity through **data-backed insights**
- Statistically validating common pricing assumptions
- Predicting a **fair expected price** for a given car configuration

---

## 🛠️ Data Collection

- Scraped real-world used-car listings from **Spinny**
- Used **Selenium** to handle dynamic content and infinite scrolling
- Parsed HTML using **BeautifulSoup** to extract:
  - Price, Year, KM Driven
  - Fuel Type, Transmission
  - Brand, Model, Variant
  - City, State
- Stored data in a structured format for analysis

---

## 🧹 Data Cleaning & Preprocessing

- Identified quantitative columns initially stored as **object (nominal) types**
- Converted **price and km** into numerical values using:
  - `replace()`, `strip()`, `mul()`, and `pd.to_numeric()`
- Handled missing and invalid values using `errors='coerce'`
- Performed **outlier detection using the IQR method**
- Standardized categorical values (fuel, transmission, state codes)

---

## 📊 Exploratory Data Analysis (EDA)

### 🔹 Univariate Analysis
- Distribution of year, price, and kilometers driven
- Frequency analysis of fuel type, transmission, brands, cities, and states

### 🔹 Bivariate Analysis
- Price vs Year (depreciation trend)
- Price vs KM Driven
- Price by Fuel Type and Transmission

### 🔹 Multivariate Analysis
- KM vs Price by Transmission
- Price distribution by Fuel & Transmission
- Correlation analysis between year, km, and price

---

## 🧪 Hypothesis Testing

Statistical tests were used to validate assumptions:

- **Correlation Tests**
  - KM vs Price
  - Year vs Price
- **t-tests / z-tests**
  - Newer cars vs older cars
  - Automatic vs manual cars
- **ANOVA**
  - Price differences across fuel types, brands, and cities
- **Chi-Square Tests**
  - Fuel vs High-Price probability
  - Transmission vs High-Price probability

Each test included **null hypothesis, alternative hypothesis, and decision logic**.

---

## 🤖 Price Prediction (Machine Learning)

- Built a **Linear Regression model** to predict used-car prices
- Applied **one-hot encoding** for categorical features
- Evaluated model using:
  - R² Score
  - MAE
  - RMSE
- Used **log-transformed price** to handle skewness and improve performance

---

## ✅ Key Insights

- Newer cars command significantly higher prices
- Higher mileage negatively impacts resale value
- Automatic cars are more likely to be high-priced
- Fuel type, brand, and location influence pricing
- Log transformation improves statistical modeling

---

## 🚀 Business Impact

- Helps buyers **avoid overpaying**
- Provides **transparent, data-driven price evaluation**
- Acts as a **decision-support system** for used-car buyers
- Demonstrates how analytics can solve real-world consumer problems

---

## 🧠 Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- SciPy, StatsModels
- Scikit-learn
- BeautifulSoup, Selenium
- Jupyter Notebook

---

## 📌 Future Enhancements

- Deploy price prediction as a web app (Streamlit)
- Add more advanced models (Random Forest, XGBoost)
- Expand dataset across multiple platforms
- Include seller-side pricing recommendations

---

## 👤 Author

**Prudhvi**  
Aspiring Data Analyst | SQL | Python | EDA | Statistics | Machine Learning  

---

## ⭐ Acknowledgment

Special thanks to mentors and learning resources that supported the completion of this project.
