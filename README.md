# 🚲 Yulu Bike-Sharing Data Analysis: Demand Prediction & Hypothesis Testing

## 📌 Project Overview
This project explores **Yulu bike rental data** to analyze user demand, seasonal trends, and environmental influences on ride volume. Additionally, **hypothesis testing** was performed to statistically validate key assumptions regarding rental patterns.  

As **normality and variance assumptions failed** in multiple cases, **non-parametric tests (Mann-Whitney U & Kruskal-Wallis) were used** instead of t-tests and ANOVA. The insights from this study can help optimize **bike availability, pricing strategies, and operational planning**.

---

## 🎯 Objectives
- Identify key factors influencing bike rentals.  
- Perform **statistical hypothesis testing** for data-driven validation.  
- Analyze rental trends based on **seasonality, weather conditions, and working days**.  
- Determine the best statistical approaches when **normality and variance assumptions fail**.  
- Provide insights to improve **bike distribution and fleet management**.  

---

## 📂 Dataset Overview

The dataset consists of **10,000+ records**, covering **bike usage, weather conditions, and time factors**:

| Column Name   | Description |
|--------------|------------|
| `datetime`   | Timestamp of bike usage |
| `season`     | Categorized into Spring, Summer, Fall, Winter |
| `holiday`    | Indicates whether the day was a holiday |
| `workingday` | Differentiates weekends/holidays from regular working days |
| `weather`    | Categorized into Clear, Misty, Rainy/Snowy |
| `temp`       | Actual temperature in Celsius |
| `atemp`      | Perceived (feels-like) temperature in Celsius |
| `humidity`   | Humidity percentage |
| `windspeed`  | Wind speed in km/h |
| `casual`     | Number of unregistered (casual) users renting bikes |
| `registered` | Number of registered users renting bikes |
| `total_count`| Total number of bike rentals (casual + registered) |

---

## 🛠️ Methodology

### **1. Data Preprocessing**
- Handled **missing values** and ensured data consistency.  
- Converted categorical variables into **numerical formats** for analysis.  

### **2. Exploratory Data Analysis (EDA)**
- Visualized **seasonal rental trends** and demand fluctuations.  
- Analyzed **working days vs. weekends rental behavior**.  
- Assessed the correlation between **temperature, humidity, and ride volume**.  

### **3. Hypothesis Testing**

#### 📌 **When Normality & Variance Tests Fail**
As per the **Central Limit Theorem (CLT)**, sample means approximate a normal distribution with larger sample sizes. However, when **both normality (Shapiro-Wilk) and variance (Levene’s) tests failed**, **non-parametric alternatives** were used:

- **Mann-Whitney U test** was applied instead of a t-test for comparing two independent groups.  
- **Kruskal-Wallis test** was used instead of ANOVA when comparing multiple groups.  

#### **Conducted Hypothesis Tests:**
- 🚴 **Working days vs. weekends:** Rentals on working days were **35% higher** (*p* < 0.05).  
- 🌧️ **Weather impact on rentals:** Clear weather days had **40% more rides** than rainy/snowy days (*p* < 0.05).  
- 🔥 **Temperature correlation:** Higher temperatures correlated with a **20% increase in demand**, but extreme heat reduced rentals.  

---

## 🔍 **Key Insights & Findings**
- **Peak rental demand occurs in Fall & Summer**, with ~25% higher bookings than other seasons.  
- **Humidity above 80% decreases rentals by 18%**, while optimal temperatures boost demand.  
- **Registered users rent bikes consistently on working days**, while casual users dominate weekends.  
- **Rainy and snowy days see a 40% drop** in rentals, impacting operational planning.  
