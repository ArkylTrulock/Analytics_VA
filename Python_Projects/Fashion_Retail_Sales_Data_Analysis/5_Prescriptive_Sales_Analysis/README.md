# 💊👗🛍️ Prescriptive Sales Analysis for Fashion Retail

![Prescriptive Sales Analysis](https://img.shields.io/badge/Analysis-Type%3A%20Prescriptive-blueviolet?labelColor=darkblue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?labelColor=crimson)
![Toolset](https://img.shields.io/badge/Toolset-Python%2C%20Apriori%2C%20Statsmodels%2C%20Seaborn-turquoise?labelColor=gold)
#
## 📌 Project Overview

This project focuses on **Prescriptive Analytics** techniques to identify **what actions to take** to optimise sales and customer retention in a fashion retail setting. Building on previous descriptive and predictive analyses, we dive into:

- 🧺 **Basket Analysis** using the **Apriori Algorithm & Association Rule Mining**  
- 📈 **Time-Based Promotional Effectiveness** a powerful tool used to drive sales, increase engagement, and achieve marketing goals. Success is contingent on careful consideration of various factors.
- 💥 **Sales Lift Analysis** comparing pre-, during-, and post-promotion periods  
- 📊 **Customer Segmentation** using **RFM (Recency, Frequency, Monetary) Analysis + CLTV (Customer lifetime value)**  
- 🧪 **Campaign Simulation & Optimisation** for targeting high-value segments

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
- **Mlxtend**: Apriori Association Rules.
- **Lifetimes**: Forecasting CLTV (Customer lifetime value)

#

## 🧠 Key Techniques & Methodologies

### 🧺 Apriori Algorithm & Association Rule Mining
- Association rule mining has become essential for businesses aiming to understand customer behaviours and purchasing patterns. 
- This technique identifies items frequently bought together, helping companies optimize product placement, promotions, and recommendations.
- Such analysis improves business strategies by clearly revealing trends hidden within transaction data.
 
### Key Metrics Evaluated
- **Support**: The frequency with which an item appears in the dataset. (`How often the rule occurs in data`) 
- **Confidence**: The likelihood that item B is purchased when item A is purchased. (`Probability of B given A`) 
- **Lift**: The strength of a rule. (`measuring how much more likely item B is bought when item A is bought compared to when bought independently`)

### **🩺 Diagnostics**:
  - Network Plots
  - Barplots

### **🔍 Insights**:
  - Lift score **`> 1`** indicates a **`strong positive association between items and not likely due to random chance`**.
  - Confidence score **`> 0.6`** indicates a **`stronger relationship between the antecedent (if purchased) and consequent (will likely be purchased) item, suggesting the rule is more reliable`**.
  - Support score **`> 0.2`** indicates a **`more frequently occurring itemset in the dataset`**. A lower score indicates a **`less frequently occuring itemset in the dataset`**.

### 📷 Visualisations

#
**Network Plot 1 - Top 10 Items Purchased - Association Rules By Lift**
![Network Plot 1 - Top 10 Items Purchased - Association Rules By Lift](../5_Prescriptive_Sales_Analysis/Assets/Py_04_Top_10_Items_Purchased_Association_Rules_By_Lift.png)  
*Generated using seaborn library*
#
**Network Plot 2 - Top 10 Items Purchased - Association Rules By Confidence And Lift**
![Network Plot 2 - Top 10 Items Purchased - Association Rules By Confidence And Lift](../5_Prescriptive_Sales_Analysis/Assets/Py_05_Top_10_Items_Purchased_Association_Rules_By_Confidence_And_Lift.png)  
*Generated using seaborn library*
#
**Barplot - Top 10 Items Purchased - Association Rules By Confidence**
![Barplot - Top 10 Items Purchased - Association Rules By Confidence](../5_Prescriptive_Sales_Analysis/Assets/Py_06_Top_10_Items_Purchased_Association_Rules_By_Confidence_Barplot.png)  
*Generated using seaborn library*
#
**Barplot - Top 10 Items Purchased - Association Rules By Lift**
![Barplot - Top 10 Items Purchased - Association Rules By Lift](../5_Prescriptive_Sales_Analysis/Assets/Py_07_Top_10_Items_Purchased_Association_Rules_By_Lift_Barplot.png)  
*Generated using seaborn library*
#

### 🛒 Time-Based Promotion Effectiveness
- Analysed impact of promotional events on sales volume
- Categorised sales into:
  - **Pre-Promotion**
  - **During Promotion**
  - **Post-Promotion**

### **🩺 Diagnostics**:
  - Line Plots

### **🔍 Insights:**

- Shaded areas indicate active promotional campaigns.
- You can observe spikes or trends in sales and ratings during these periods.
- Helps evaluate campaign success visually.

### 📷 Visualisations

#
**Lineplot - Time-Based Promotional Effectiveness**
![Lineplot - Time-Based Promotional Effectiveness](../5_Prescriptive_Sales_Analysis/Assets/Py_08_Time_Based_Promotional_Effectiveness_Sales_&_Review_Ratings_Linelot.png)  
*Generated using seaborn library*
#
**Lineplot - Time-Based Promotional Effectiveness With Promotion Overlays**
![Lineplot - Time-Based Promotional Effectiveness With Promotion Overlays](../5_Prescriptive_Sales_Analysis/Assets/Py_09_Time_Based_Promotional_Effectiveness_Sales_&_Review_Ratings_Linelot.png)  
*Generated using seaborn library*
#

### 📉 Sales Lift Analysis (Pre vs During vs Post Promotion)
- Quantified the **true effectiveness** of promotions
- Metrics included:  
  - Absolute sales change  
  - Relative % improvement  
  - Baseline vs. uplift performance

### **🧮 Lift Math**:
- Lift vs Pre (%) = ((During - Pre) / Pre) × 100
- Lift vs Post (%) = ((During - Post) / Post) × 100

### **🩺 Diagnostics**:
  - Barplot

### 🖼️ Results Snapshot
|Promotion|Pre_Sales|During_Sales|Post_Sales|Lift_vs_Pre(%)|Lift_vs_Post(%)|
|---------|---------|------------|----------|--------------|---------------|
Summer Sale|0.0|0.0|0.0|N/A|N/A|
Black Friday|$ 20,474.0|$ 4,263.0|$ 20,689.0|🔻-79.18 %|🔻-79.39 %|
End-of-Year Sale|$ 26,798.0|$ 22,311.0|$ 13,361.0|🔻-16.74 %|🔼66.99 %|

### **🔍 Insights:**

- **Summer Sale**: No data available for analysis.
- **Black Friday**: Sales significantly dropped during the promotion compared to both pre and post periods.
- **End-of-Year Sale**: Slight drop during the promotion vs pre-period, but significantly higher than post-period → demand likely pulled forward.

### 📷 Visualisation

#
**Barplot - Sales Lift Analysis: Pre Vs During Vs Post Promotion**
![Barplot - Sales Lift Analysis: Pre Vs During Vs Post Promotion](../5_Prescriptive_Sales_Analysis/Assets/Py_10_Sales_Lift_Analysis_Pre_Vs_During_Vs_Post_Promotion_Barplot.png)  
*Generated using seaborn library*
#

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
