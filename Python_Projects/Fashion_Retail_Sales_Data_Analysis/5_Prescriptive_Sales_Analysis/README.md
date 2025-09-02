# 💊👗🛍️ Prescriptive Sales Analysis for Fashion Retail

![Prescriptive Sales Analysis](https://img.shields.io/badge/Analysis-Type%3A%20Prescriptive-blueviolet?labelColor=darkblue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?labelColor=crimson)
![Toolset](https://img.shields.io/badge/Toolset-Pandas%2C%20Apriori%2C%20Statsmodels%2C%20Seaborn%2C%20Scikitlearn%2C%20Statsmodels%2C%20Mlxtend%2C%20Lifetimes-turquoise?labelColor=gold)
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
- **Lifetimes**: Forecasting CLTV (Customer lifetime value).

#

## 🧠 Key Techniques & Methodologies

### 🧺 Apriori Algorithm & Association Rule Mining
- Association rule mining has become essential for businesses aiming to understand customer behaviours and purchasing patterns. 
- This technique identifies items frequently bought together, helping companies optimize product placement, promotions, and recommendations.
- Such analysis improves business strategies by clearly revealing trends hidden within transaction data.
 
### Key Metrics Evaluated
- **Support**: The frequency with which an item appears in the dataset. **(`How often the rule occurs in data`)** 
- **Confidence**: The likelihood that item B is purchased when item A is purchased. **(`Probability of B given A`)**
- **Lift**: The strength of a rule. **(`measuring how much more likely item B is bought when item A is bought compared to when bought independently`)**

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
  - Line Plots.

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
- Quantified the **true effectiveness** of promotions.
- Metrics included:  
  - Absolute sales change.
  - Relative % improvement.
  - Baseline vs. uplift performance.

### 🧮 Lift Math
- Lift vs Pre (%) = ((During - Pre) / Pre) × 100
- Lift vs Post (%) = ((During - Post) / Post) × 100

### **🩺 Diagnostics**
  - Barplot.

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

### Customer Segmentation Using RFM Analysis And K-Means Clustering With Targeting Strategy And Marketing Channels

#### What is K-Means Clustering?
- Unsupervised machine learning technique that allows the identification of clusters (similar groups of data points) within the data.

### Key Metrics Evaluated

#### RFM Analysis
- Calculated **`RFM metrics`** per customer.
  - **Recency**: Days since last purchase (how recently the customer bought).
  - **Frequency**: Total number of purchases.
  - **Monetary**: Total spending.

- Scored each RFM metric on a scale of **`1`** to **`5`** using quantiles.
  - Higher scores indicate better performance, except Recency (lower is better).

- Combined the RFM metric scores into **`RFM Segment`**.

- Calculated the **`RFM Score`** totals by summing the values in **`RFM Segment`**.

#### K-Means Clustering
- Selected only the numerical features of the RFM metrics, standardised data and chose the optimal number of clusters **`(k = 4)`** using the **`Elbow Method`**.
  - The **`k value`** corresponding to the **`"elbow"`** in the WCSS vs k graph is considered the optimal choice.

- Grouped RFM metrics by cluster and calculated :
  - Mean RFM metric scores.
  - Customer counts.

### Dataframe Columns
  - **`Cluster`**: **3**, **2**, **1** and **0**.
  - **`Customer_Count`**: **The total number of customers**.
  - **`Recency`**: **Mean days since last purchase**.
  - **`Frequency`**: **Mean number of purchases**.
  - **`Monetary`**: **Mean total spending**.
  - **`RFM_Score`**: **Mean metric score**.
  - **`Profile summary`**: **"Champions"**, **"Loyal"**, **"Potential"**, **"At Risk"** and **"Lost"**.
  - **`Customer Value`**: **"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**.
  - **`Recommended Strategy`**: 
    - **Exclusive offers, loyalty rewards**.  
    - **Early access, product sneak peeks**.
    - **Nurture campaigns, discounts, product education**.
    - **Re-engagement offers, feedback surveys**.
    - **Win-back with bold offers, remove after attempts**.
  - **`Marketing Channel`**: 
    - **Email, VIP newsletters, App push.**. 
    - **SMS, Email drip campaigns, Loyalty app.**.
    - **Retargeting Ads, Email, Social media**.
    - **Email reactivation, Discount codes, SMS**.
    - **Paid Ads, Remarketing, Personalised mail**.
    
### **🩺 Diagnostics**
  - Line Plots.
  - Barplot.
  - Scatterplots.

### 🖼️ Results Snapshot
|Cluster|Recency|Frequency|Customer_Count|Monetary|RFM_Score|Profile Summary|Customer Value|Recommended Strategy|Marketing Channel|
|-------|-------|---------|--------------|--------|---------|---------------|--------------|--------------------|------|
|0|13.83|16.69|54|$ 2,039.30|7.04|🔃 New / Promising|🥉 Medium|Nurture campaigns, discounts, product education.|Retargeting Ads, Email, Social media.|
|1|58.32|17.32|22|$ 2,087.50|4.77|❗At-Risk / Churned|🎁 Low|Re-engagement offers, feedback surveys.|Email reactivation, Discount codes, SMS.|
|2|12.89|23.71|63|$ 2,679.35|11.11|✅ Loyal Customers|🥈 Medium-High|Early access, product sneak peeks.|SMS, Email drip campaigns, Loyalty app.|
|3|16.04|23.11|27|$ 6,495.81|11.89|💎 Champions / VIP|🥇 Very High|Exclusive offers, loyalty rewards.|Email, VIP newsletters, App push.|

### **🔍 Insights**
 - **TBC**.

### 📷 Visualisation

#
**Lineplot - K-Means Clustering - Identifying The Optimal Number Of Clusters `(k)` Using The Elbow Method**
![Lineplot - K-Means Clustering - Identifying The Optimal Number Of Clusters (k) Using The Elbow Method](../5_Prescriptive_Sales_Analysis/Assets/Py_12_Identifying_The_Optimal_Number_Of_Clusters_k_Using_The_Elbow%20Method_Line_Plot.png)  
*Generated using seaborn library*
#
**Barplot - RFM Metric Scores, Customer Count, Customer Value, Profile Summary, Recommended Strategy And Marketing Channel Of KMeans Clusters**
![Barplot - RFM Metric Scores, Customer Count, Customer Value, Profile Summary, Recommended Strategy And Marketing Channel Of KMeans Clusters](../5_Prescriptive_Sales_Analysis/Assets/Py_15_RFM_Metric_Scores_Cust_Count_Cust_Value_Prof_Summary_Recommended_Strategy_Marketing_Channel_Of_KMeans_Clusters_Barplot.png)  
*Generated using seaborn library*
#
**Scatterplot - Customer Segments - Recency Vs Frequency**
![Scatterplot - Customer Segments - Recency Vs Frequency](../5_Prescriptive_Sales_Analysis/Assets/Py_16_Customer_Segments_Recency_Vs_Frequency_Scatterplot.png)  
*Generated using seaborn library*
#
**Scatterplot - Customer Segments - Recency Vs Monetary**
![Scatterplot - Customer Segments - Recency Vs Monetary](../5_Prescriptive_Sales_Analysis/Assets/Py_17_Customer_Segments_Recency_Vs_Monetary_Scatterplot.png)  
*Generated using seaborn library*
#
**Scatterplot - Customer Segments - Frequency Vs Monetary**
![Scatterplot - Customer Segments - Frequency Vs Monetary](../5_Prescriptive_Sales_Analysis/Assets/Py_18_Customer_Segments_Frequency_Vs_Monetary_Scatterplot.png)  
*Generated using seaborn library*
#

### **🔍 Insights**
 - **TBC**.

#

### 📦 Predicted 6-Month CLTV - Customer Segmentation Using RFM Analysis And K-Means Clustering With Targeting Strategy And Marketing Channels

#### What is CLTV (Customer Lifetime Value)?
- A **`monetary value`** that represents the **`amount of revenue or profit a customer will give the company over the period of the relationship`**.

- A technique used to forecast the total revenue a business expects to generate from a single customer relationship over their entire lifespan.

#### Why is it important?
- It helps businesses understand the long-term value of their customers, enabling them to make more informed decisions about customer acquisition, retention, and marketing strategies.

### Key Metrics Evaluated

#### 6-Month CLTV
 - The CLTV for 6 months was predicted using `lifetimes` library.

#### RFM Analysis
 - Please refer to notes above.

#### K-Means Clustering
 - Please refer to notes above.

### Dataframe Columns
- **`customer_reference_id`**: **Self explanatory**.
- **`Recency`**: **Days since last purchase**.
- **`Frequency`**: **Number of purchases**.
- **`Monetary`**: **Total spending**.
- **`R_Score`**: **Recency score**.
- **`F_Score`**: **Frequency score**.
- **`M_Score`**: **Monetary score**.
- **`RFM_Segment`**: **Recency + Frequency + Monetary score**.
- **`Cluster`**: **3**, **2**, **1** and **0**.
- **`predicted_cltv_6m`**: **The predicted CLTV for 6 months**.
- **`cltv_segment`**:	**: **"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**.
- **`cltv_strategy`**:
    - **Retain + Reward**.
    - **Upsell + Personalise**.
    - **Educate + Re-target**.
    - **Incentivise + Survey**.
    - **Re-engage + Exit**.
- **`cltv_marketing_channel`**:
    - **Email, SMS, App Push, 1:1 service**.   
    - **Email, Paid Ads, Mobile App**.
    - **Email Series, Blog, Social Media**.
    - **Email, Push Notification**.
    - **Email, Re-targeting Ads**.

### **🩺 Diagnostics**
  - Dataframes.
 
### 🖼️ Results Snapshot
#
**Dataframe - Predicted 6-Month CLTV - Customer Segmentation Using RFM Analysis With Targeting Strategy And Marketing Channels**
![Dataframe - Predicted 6-Month CLTV - Customer Segmentation Using RFM Analysis With Targeting Strategy And Marketing Channels](../5_Prescriptive_Sales_Analysis/Assets/Py_26_Predicted_6_Month_CLTV_Customer_Segmentation_Using_RFM_Analysis_With_T_S_And_M_C.png)  
*Generated using pandas library*
#

### Statistical Analysis Of The Predicted 6-Month CLTV
 - A statistical analysis was done on the predicted CLTV for 6 months.

### Key Metrics Evaluated
1) Descriptive Statistics Of Predicted 6-Month CLTV By **`Cluster`**.
2) Descriptive Statistics Of Predicted 6-Month CLTV By **`Segment`**.
3) Descriptive Statistics Of Predicted 6-Month CLTV By **`Strategy`**.

### Dataframe Columns
- **`Cluster`**: **3**, **2**, **1** and **0**.
- **`Count`**: **The total number of customers**.
- **`avg_predicted_cltv_6m`**: **The mean predicted CLTV for 6 months**.
- **`median_predicted_cltv_6m`**: **The median predicted CLTV for 6 months**.
- **`min_predicted_cltv_6m`**: **The minimum predicted CLTV for 6 months**.
- **`max_predicted_cltv_6m`**: **The maximum predicted CLTV for 6 months**.
- **`cltv_segment`**:	**: **"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**.
- **`cltv_strategy`**:
    - **Retain + Reward**.
    - **Upsell + Personalise**.
    - **Educate + Re-target**.
    - **Incentivise + Survey**.
    - **Re-engage + Exit**.

### **🩺 Diagnostics**
  - Dataframes.

### 📷 Visualisation

#
**Dataframe - Descriptive Statistics Of Predicted 6-Month CLTV By Cluster**
![Dataframe - Descriptive Statistics Of Predicted 6-Month CLTV By Cluster](../5_Prescriptive_Sales_Analysis/Assets/Py_27_Descriptive_Statistics_Of_Predicted_6_Month_CLTV_By_Cluster.png)  
*Generated using pandas library*
#
**Dataframe - Descriptive Statistics Of Predicted 6-Month CLTV By Segment**
![Dataframe - Descriptive Statistics Of Predicted 6-Month CLTV By Segment](../5_Prescriptive_Sales_Analysis/Assets/Py_28_Descriptive_Statistics_Of_Predicted_6_Month_CLTV_By_Segment.png)  
*Generated using pandas library*
#
**Dataframe - Descriptive Statistics Of Predicted 6-Month CLTV By Strategy**
![Dataframe - Descriptive Statistics Of Predicted 6-Month CLTV By Strategy](../5_Prescriptive_Sales_Analysis/Assets/Py_29_Descriptive_Statistics_Of_Predicted_6_Month_CLTV_By_Strategy.png)  
*Generated using pandas library*
#

### **🔍 Insights**
 - **TBC**.

#

### Distribution Overview Of The Predicted 6-Month CLTV
 - A distribution overview was done on the predicted CLTV for 6 months.

### Key Metrics Evaluated
1) Distribution Of Predicted 6-Month CLTV.
2) Distribution Of Predicted 6-Month CLTV By **`Cluster`**.
3) Distribution Of Predicted 6-Month CLTV By **`Segment`**.
4) Distribution Of Predicted 6-Month CLTV By **`Strategy`**.
5) Distribution Of Predicted 6-Month CLTV By **`Segment (Strategy & Marketing Channel Included)`**.

### **🩺 Diagnostics**
  - Hisplots.
  - Boxplots.

### 📷 Visualisation

#
**Hisplot - Distribution Of Predicted 6-Month CLTV**
![Hisplot - Distribution Of Predicted 6-Month CLTV By Cluster](../5_Prescriptive_Sales_Analysis/Assets/Py_30_Distribution_Of_Predicted_6_Month_CLTV_Histplot.png)  
*Generated using seaborn library*
#
**Hisplot - Distribution Of Predicted 6-Month CLTV By Cluster**
![Hisplot - Distribution Of Predicted 6-Month CLTV By Cluster](../5_Prescriptive_Sales_Analysis/Assets/Py_31_Distribution_Of_Predicted_6_Month_CLTV_By_Cluster_Histplot.png)  
*Generated using seaborn library*
#
**Hisplot - Distribution Of Predicted 6-Month CLTV By Segement**
![Hisplot - Distribution Of Predicted 6-Month CLTV By Segment](../5_Prescriptive_Sales_Analysis/Assets/Py_32_Distribution_Of_Predicted_6_Month_CLTV_By_Segment_Histplot.png)  
*Generated using seaborn library*
#
**Hisplot - Distribution Of Predicted 6-Month CLTV By Strategy**
![Hisplot - Distribution Of Predicted 6-Month CLTV By Strategy](../5_Prescriptive_Sales_Analysis/Assets/Py_33_Distribution_Of_Predicted_6_Month_CLTV_By_Strategy_Histplot.png)  
*Generated using seaborn library*
#
**Boxplot - Distribution Of Predicted 6-Month CLTV By Cluster**
![Boxplot - Distribution Of Predicted 6-Month CLTV By Cluster](../5_Prescriptive_Sales_Analysis/Assets/Py_34_Distribution_Of_Predicted_6_Month_CLTV_By_Cluster_Boxplot.png)  
*Generated using seaborn library*
#
**Boxplot - Distribution Of Predicted 6-Month CLTV By Segment (Strategy & Marketing Channel Included)**
![Boxplot - Distribution Of Predicted 6-Month CLTV By Cluster (Strategy & Marketing Channel Included)](../5_Prescriptive_Sales_Analysis/Assets/Py_35_Distribution_Of_Predicted_6_Month_CLTV_By_Segment_Boxplot.png)  
*Generated using seaborn library*
#
**Boxplot - Distribution Of Predicted 6-Month CLTV By Strategy**
![Boxplot - Distribution Of Predicted 6-Month CLTV By Strategy](../5_Prescriptive_Sales_Analysis/Assets/Py_36_Distribution_Of_Predicted_6_Month_CLTV_By_Strategy_Boxplot.png)  
*Generated using seaborn library*
#

### **🔍 Insights**
 - **TBC**.
#

### Campaign Simulation And ROI Estimation Using Predicted CLTV Segments

#### What Is ROI (Return on Investment)?
 - A **`performance metric`** that measures the **`profitability of an investment`**.

 - It indicates how much return is generated relative to the cost of the investment.

#### Why is it important?
 - By understanding the CLTV, businesses can make more **`informed decisions`** about **`how much to spend`** on **`acquiring`** and **`retaining customers`** to **`maximise`** their overall **`ROI`**.

 - By comparing the cost of acquiring a customer (CAC) and their CLTV, you can assess your ROI.

### Key Metrics Evaluated
 - **`Response Rate`**
 - **`Cost Per Customer`**
 - **`Expected Response`**
 - **`Expected Revenue`**
 - **`Total Cost`**
 - **`Profit`**
 - **`ROI %`**

### 🧮 Financial Math
 - Response Rate = Customer response value to simulated campaign
 - Cost Per Customer = Customer aquisition cost
 - Expected Response = Customers * Response Rate
 - Expected Revenue = Expected_responses * Mean 6-month CLTV * Response Rate
 - Total Cost = Customers * Cost Per Customer
 - Profit = Expected Revenue - Total Cost
 - ROI % = (Expected Revenue - Total Cost) / (Total Cost * 100)

### Dataframe Columns
- **`cltv_segment`**:	**: **"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**.
- **`avg_cltv`**: **The mean predicted CLTV for 6 months**.
- **`Customers`**: **The total number of customers**.
- **`cost_per_customer`**: **The aquisition cost per customer**.
- **`total_cost`**: **The total cost of aquiring customers**.
- **`expected_revenue`**: **Estimate of how much money the business expects to earn over a specific period—whether that's a month, a quarter, or a full year.**.
- **`profit`**: **The money you have left after paying for business expenses. There are three main types of profit: gross profit, operating and net profit.**.
- **`roi_percent`**: **The return on investment expressed as a percentage**.

### **🩺 Diagnostics**
  - Dataframe.

### 📷 Visualisation

#
**Dataframe - Campaign Simulation And ROI Estimation Using Predicted CLTV Segments**
![Dataframe - Campaign Simulation And ROI Estimation Using Predicted CLTV Segments](../5_Prescriptive_Sales_Analysis/Assets/Py_37_Campaign_Simulation_And_ROI_Estimation_Using_Predicted_CLTV_Segments.png)  
*Generated using pandas library*
#

### **🔍 Insights**
 - **TBC**.

#

### 🎯 Campaign Optimisation
- Targeting rules built using RFM + CLTV outputs
- Simulated campaign strategies for uplift impact
- Laid foundation for **A/B testing** and **Uplift Modeling**

#

## 📬 Contact
*Built by [Arkyl Trulock](https://github.com/ArkylTrulock)*  
For collaborations or feedback: X@gmail.com 