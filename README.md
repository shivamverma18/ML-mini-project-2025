# 🏨 Hotel Booking Prediction — Machine Learning Mini Project  
### 📌 Author: **Shivam Verma (PRN: 22070521132)**  
### 📚 Course: Machine Learning (CA4)  
### 🏫 Symbiosis Institute of Technology, Nagpur  
### 👨‍🏫 Guided by: **Dr. Piyush Chauhan**

---

## 📘 Project Overview

This project focuses on predicting key patterns in hotel bookings using Machine Learning techniques.  
The dataset includes multiple interconnected files related to booking transactions, hotel metadata, room categories, and date dimensions.

The project includes:

- ✔️ Exploratory Data Analysis (EDA)  
- ✔️ Data Cleaning & Feature Engineering  
- ✔️ Training 12 Machine Learning Models  
- ✔️ Model Evaluation & Comparison  
- ✔️ Business Insights & Recommendations  

This helps understand hotel performance, customer behavior, occupancy patterns, and booking trends.

---

## 📂 Dataset Description

The analysis uses **five CSV datasets**:

| File Name | Description |
|-----------|-------------|
| `original_bookings_data.csv` | Booking details including dates, guests, revenue, room type, platform |
| `fact_aggregated_bookings.csv` | Aggregated data: successful bookings & capacity |
| `dim_hotels.csv` | Hotel metadata (property name, category, city) |
| `dim_rooms.csv` | Room ID & room type mapping |
| `dim_date.csv` | Calendar details: day type, month-year, week number |

### 🧮 Dataset Size
- **Total rows (merged): ~118,950**  
- **Total columns: ~32**

### 🔑 Key Variables
`booking_id`, `property_id`, `room_category`, `booking_date`, `check_in_date`,  
`checkout_date`, `no_guests`, `booking_platform`, `booking_status`,  
`revenue_realized`, `revenue_generated`, `city`, `category`,  
`capacity`, `successful_bookings`, `day_type`, `booking_month_year`

---

## 🧹 Data Cleaning & Feature Engineering

### ✔️ Handling Invalid / Missing Values
- Converted **negative guest counts** to positive using `.abs()`
- Filled missing `no_guests` using **median**
- Dropped `ratings_given` (58% missing)
- Fixed outlier revenue entries by aligning `revenue_generated` with `revenue_realized` when values were unrealistic

### ✔️ Date Standardization
Used custom function `parse_date_robust` to handle formats:
- `%Y-%m-%d`
- `%d-%m-%Y`
- `%d/%m/%Y`
- `%d-%b-%y`

Ensured uniform `YYYY-MM-DD` format.

### ✔️ Fact Table Cleaning
- Missing `capacity` fixed with median
- Standardized all date fields

### ✔️ Feature Engineering
- Created `occ_pct = (successful_bookings / capacity) * 100`
- Extracted `booking_month_year` from dates
- Mapped room categories to:
  - Standard  
  - Elite  
  - Premium  
  - Presidential

---

## 📊 Exploratory Data Analysis (EDA)

### ✔ 1. Occupancy Analysis
- Premium & Elite rooms show higher occupancy
- Clear demand patterns per room type

### ✔ 2. Top Performing Hotels
- Hotels in metro cities show higher occupancy
- Property-level variations observed

### ✔ 3. Revenue by Booking Platform
- Platforms contributing highest revenue:  
  **Direct Online**, **Makeyourtrip**, **Tripster**

### ✔ 4. Revenue by Hotel Category
- **Luxury hotels** generate more revenue than Business category

### ✔ 5. Monthly Revenue Trends
- Clear seasonality in booking and revenue patterns

### ✔ 6. Capacity Utilization Across Cities
- Some hotels underutilize capacity
- Some operate close to full capacity consistently

### ✔ 7. Weekday vs Weekend Revenue
- Weekends show slightly higher median revenue values

---

## 🤖 Machine Learning Models Used

A total of **12 ML models** were trained:

- Logistic Regression  
- KNN Classifier  
- Support Vector Machine (SVM)  
- Decision Tree  
- Random Forest  
- SGD Classifier  
- Bernoulli Naive Bayes  
- Gaussian Naive Bayes  
- Gradient Boosting Classifier  
- AdaBoost Classifier  
- Trees Classifier  

---

## 🏆 Model Performance Summary

### ⭐ **Best Performing Model**
#### **Gradient Boosting Classifier**
- Accuracy: **93%**
- Precision: **92%**
- ROC-AUC: **94%**

### ⭐ Strong Contenders
- **Random Forest**
- **AdaBoost**

### ⭐ Baseline Models
- Logistic Regression  
- SVM  
- Naive Bayes  

---

## 🚀 Future Scope

- Add **Deep Learning models (ANN, LSTM)**  
- Apply **Hyperparameter tuning & Cross-validation**  
- Build **Customer Segmentation using K-Means**  
- Create a **Recommendation System**  
- Apply **NLP for review sentiment analysis**  
- Build an **Interactive Dashboard (Power BI / Streamlit)**  

---

📁 Project
 ├── 📁 Cleaned Datasets
 ├── 📁 Original Datasets
 ├── 📁 EDA Task1
 ├── 📁 ML Algorithm Task2
 └── README.md


---

## 🛠️ Tech Stack

- **Python 3**  
- **pandas, numpy**  
- **matplotlib, seaborn, plotly**  
- **scikit-learn**  
- **Jupyter Notebook**

---

## 📫 Contact

**Shivam Verma**  
📧 Email: *shivamgverma99@gmail.com*  


---

