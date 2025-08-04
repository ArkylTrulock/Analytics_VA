# 🧠 Prescriptive Sales Analysis for Fashion Retail

![Prescriptive Sales Analysis](https://img.shields.io/badge/Analysis-Type%3A%20Prescriptive-blueviolet?labelColor=darkblue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?labelColor=crimson)
![Toolset](https://img.shields.io/badge/Toolset-Python%2C%20Apriori%2C%20Statsmodels%2C%20Seaborn-turquoise?labelColor=gold)
#
## 📌 Project Overview

This project focuses on **Prescriptive Analytics** techniques to identify **what actions to take** to optimize sales and customer retention in a fashion retail setting. Building on previous descriptive and predictive analyses, we dive into:

- 🧺 **Basket Analysis** using the **Apriori algorithm**  
- 📈 **Promotion Effectiveness** based on temporal windows  
- 💥 **Sales Lift Analysis** comparing pre-, during-, and post-promotion periods  
- 📊 **Customer Segmentation** using **RFM Analysis + CLTV**  
- 🧪 **Campaign Simulation & Optimization** for targeting high-value segments

#

## 🧰 Tech Stack
- Python (`pandas`, `numpy`, `seaborn`, `sklearn`, `statsmodels`,`prophet`, `pmdarima`, `networkx`, `mlxtend`, `lifetimes`)  
- Jupyter Notebook 

#

## 🧠 Methods & Tools
### **Python Libraries**:

- **Pandas**: Data analysis and manipulation. 
- **Numpy**: Scientific computing.  
- **Seaborn**: Statistical data visualisation.
- **Scikit-learn**: Clustering and uplift modeling.
- **Statsmodels**: Statistical modeling and forecasting.
- **Networkx**: Creation, manipulation, and study of the structure, dynamics, and functions of complex networks.
- **Mlxtend (Machine Learning Extensions)**: Apriori Association Rules.
- **Lifetimes**: Forecasting the total revenue a business expects to generate from a single customer relationship over their entire lifespan.

#

## 🔍 Key Techniques & Methodologies

### 🧺 Association Rule Mining (Apriori)
- Used to find frequently co-purchased product sets
- Generates actionable rules like:  
  `If {Product A, Product B}, then {Product C}`  
- Metrics evaluated: **support**, **confidence**, **lift**

### 🛒 Time-Based Promotion Effectiveness
- Analysed impact of promotional events on sales volume
- Categorised sales into:
  - **Pre-Promotion**
  - **During Promotion**
  - **Post-Promotion**

### 📉 Sales Lift Analysis
- Quantified the **true effectiveness** of promotions
- Metrics included:  
  - Absolute sales change  
  - Relative % improvement  
  - Baseline vs. uplift performance

### 📦 RFM Segmentation + CLTV
- **Recency**, **Frequency**, and **Monetary** values used to segment customers
- Combined with **Historical CLTV** to estimate customer value
- Result:
  - Profiled RFM: **3**, **2**, **1** and **0**
  - Profiled RFM segments: **"Champions"**, **"Loyal"**, **"Potential"**, **"At Risk"** and **"Lost"**
  - Profiled cltv segments: **"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**
  - Profiled cltv strategies: **"Retain + Reward"**, **"Upsell + Personalise"**, **"Educate + Re-target"**, **"Incentivise + Survey"** and **"Re-engage + Exit"**
  - Profiled cltv marketing channels: **"Email, SMS, App Push, 1:1 service"**, **"Email, Paid Ads, Mobile App"**, **"Email Series, Blog, Social Media"**, **"Email, Push Notification"** and **"Email, Re-targeting Ads"**

### 🎯 Campaign Optimisation
- Targeting rules built using RFM + CLTV outputs
- Simulated campaign strategies for uplift impact
- Laid foundation for **A/B testing** and **Uplift Modeling**
