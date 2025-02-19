# Zomato Dataset Cleaning Project  

## 📌 Project Overview  
This project focuses on cleaning and preprocessing the **Zomato dataset** to make it suitable for analysis. The dataset is sourced from **Kaggle** and contains restaurant-related information such as ratings, votes, cost for two people, cuisines, and more. The goal is to handle missing values, correct formatting issues, and ensure data consistency.  

---

## 📂 Dataset Information  
- **Source:** Kaggle  
- **File Format:** CSV  
- **Key Columns:**
  - `URL` - Link to the restaurant  
  - `ADDRESS` - Restaurant location  
  - `NAME` - Name of the restaurant  
  - `ONLINE_ORDER` - Whether online ordering is available  
  - `BOOK_TABLE` - Whether table booking is available  
  - `RATE` - Restaurant rating  
  - `VOTES` - Number of votes  
  - `CUISINES` - Types of cuisines offered  
  - `APPROX_COST_FOR_TWO_PEOPLE` - Estimated cost for two people  

---

## 🛠 Data Cleaning Steps  
### ✔ 1. Handling Missing Values  
- Columns like `PHONE`, `DISH_LIKED`, `APPROX_COST_FOR_TWO_PEOPLE` had missing values.  
- Used **median imputation** for numerical values and **mode imputation** for categorical values.  
- Filled missing ratings (`RATE`) with `"Not Rated"` where necessary.  

### ✔ 2. Formatting and Standardization  
- Removed unnecessary characters from **column names** (e.g., replaced `()`, spaces, and special characters).  
- Standardized the `RATE` column to **one decimal place** and appended `"out of 5"`.  
- Converted `APPROX_COST_FOR_TWO_PEOPLE` to **integer values** after removing commas.  

### ✔ 3. Removing Duplicates  
- Used `data.duplicated().sum()` to check for duplicate rows.  
- Removed duplicate entries to ensure data integrity.  

### ✔ 4. Saving the Cleaned Data  
- The cleaned dataset is saved as:
  - **CSV Format:** `Cleaned_zomato_dataset.csv`  
  - **Excel Format:** `Cleaned_zomato_dataset.xlsx`  

---

## 📦 Technologies Used  
- **Python** 🐍  
- **Pandas** 📊  
- **NumPy** 🔢  
- **OpenPyXL** (for Excel export) 📂  

---

## Download dataset From kaggle
https://www.kaggle.com/datasets/rishikeshkonapure/zomato

## Results and insights
- Cleaned dataset ready for analysis.
- Improved data quality by handling missing and inconsistent data.
- Prepared dataset for further data analysis and visualization
