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
- Top 10 Product Pairing Recommendations Based On Customer Purchase Behaviour.
- Top 10 Items Purchased - Association Rules By Lift.
- Top 10 Items Purchased - Association Rules By Confidence And Lift.
- Top 10 Items Purchased - Association Rules By Confidence

### **🩺 Diagnostics**:
  - Dataframe.
  - Network Plots.
  - Barplots.

### 🖼️ Results Snapshot

**Top 10 Product Pairing Recommendations Based On Customer Purchase Behaviour**.
#
|customer_reference_id|antecedents|                      consequents|                       support|   confidence|  lift|
|--|--|--|--|--|--|
1002120|        (Loafers, Vest, Leggings, Blouse)|            (Dress, Trousers, Camisole)|  0.024096|         1.0|  41.5|
1002169|              (Dress, Trousers, Camisole)|      (Loafers, Vest, Leggings, Blouse)|  0.024096|         1.0|  41.5|
1004403|     (Gloves, Onesie, Trousers, Camisole)|             (Jumpsuit, Vest, Tank Top)|  0.024096|         1.0|  41.5|
1004422|               (Jumpsuit, Vest, Tank Top)|   (Gloves, Onesie, Trousers, Camisole)|  0.024096|         1.0|  41.5|
1011377|         (Wallet, Blouse, Blazer, Poncho)|     (Handbag, Jeans, Kimono, Cardigan)|  0.024096|         1.0|  41.5|
1011379|         (Wallet, Kimono, Blazer, Poncho)|     (Blouse, Handbag, Jeans, Cardigan)|  0.024096|         1.0|  41.5|
1011434|       (Blouse, Handbag, Jeans, Cardigan)|       (Wallet, Kimono, Blazer, Poncho)|  0.024096|         1.0|  41.5|
1011436|       (Handbag, Jeans, Kimono, Cardigan)|       (Wallet, Blouse, Blazer, Poncho)|  0.024096|         1.0|  41.5|
1011643|      (Jacket, Blazer, Cardigan, Sandals)|  (Wallet, Handbag, Poncho, Flip-Flops)|  0.024096|         1.0|  41.5|
1011649|  (Jacket, Handbag, Flip-Flops, Cardigan)|      (Wallet, Blazer, Poncho, Sandals)|  0.024096|         1.0|  41.5|
#
 
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

### **🔍 Insights**:
  - Lift score **`> 1`** indicates a **`strong positive association between items and not likely due to random chance`**.
  - Confidence score **`> 0.6`** indicates a **`stronger relationship between the antecedent (if purchased) and consequent (will likely be purchased) item, suggesting the rule is more reliable`**.
  - Support score **`> 0.2`** indicates a **`more frequently occurring itemset in the dataset`**. A lower score indicates a **`less frequently occuring itemset in the dataset`**.

#

### 🛒 Time-Based Promotion Effectiveness
- Analysed impact of promotional events on sales volume
- Categorised sales into:
  - **Pre-Promotion**
  - **During Promotion**
  - **Post-Promotion**

### Key Metrics Evaluated
1) Time-Based Promotional Effectiveness.
2) Time-Based Promotional Effectiveness With Promotion Overlays.

### **🩺 Diagnostics**:
  - Line Plots.
 
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

### **🔍 Insights:**
 - Shaded areas indicate active promotional campaigns.
 - You can observe spikes or trends in sales and ratings during these periods.
 - Helps evaluate campaign success visually.

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

**Sales Lift Analysis: Pre Vs During Vs Post Promotion**.
#
|Promotion|Pre_Sales|During_Sales|Post_Sales|Lift_vs_Pre(%)|Lift_vs_Post(%)|
|---------|---------|------------|----------|--------------|---------------|
Summer Sale|0.0|0.0|0.0|N/A|N/A|
Black Friday|$ 20,474.0|$ 4,263.0|$ 20,689.0|🔻-79.18 %|🔻-79.39 %|
End-of-Year Sale|$ 26,798.0|$ 22,311.0|$ 13,361.0|🔻-16.74 %|🔼66.99 %|
#
 
### 📷 Visualisation

#
**Barplot - Sales Lift Analysis: Pre Vs During Vs Post Promotion**
![Barplot - Sales Lift Analysis: Pre Vs During Vs Post Promotion](../5_Prescriptive_Sales_Analysis/Assets/Py_10_Sales_Lift_Analysis_Pre_Vs_During_Vs_Post_Promotion_Barplot.png)  
*Generated using seaborn library*
#

### **🔍 Insights:**

- **Summer Sale**: No data available for analysis.
- **Black Friday**: Sales significantly dropped during the promotion compared to both pre and post periods.
- **End-of-Year Sale**: Slight drop during the promotion vs pre-period, but significantly higher than post-period → demand likely pulled forward.

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
  - **`Recency`**: **The number of days since last purchase**.
  - **`Frequency`**: **The number of purchases**.
  - **`Monetary`**: **The total revenue/profit generated**.
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
  - Heatmap.
  - Countplot.
  - Scatterplot.

### 🖼️ Results Snapshot

**RFM Metric Scores, Customer Count, Customer Value, Profile Summary, Recommended Strategy And Marketing Channel Of KMeans Clusters**.
#
|Cluster|Recency|Frequency|Customer_Count|Monetary|RFM_Score|Profile Summary|Customer Value|Recommended Strategy|Marketing Channel|
|-------|-------|---------|--------------|--------|---------|---------------|--------------|--------------------|------|
|0|13.83|16.69|54|$ 2,039.30|7.04|🔃 New / Promising|🥉 Medium|Nurture campaigns, discounts, product education.|Retargeting Ads, Email, Social media.|
|1|58.32|17.32|22|$ 2,087.50|4.77|❗At-Risk / Churned|🎁 Low|Re-engagement offers, feedback surveys.|Email reactivation, Discount codes, SMS.|
|2|12.89|23.71|63|$ 2,679.35|11.11|✅ Loyal Customers|🥈 Medium-High|Early access, product sneak peeks.|SMS, Email drip campaigns, Loyalty app.|
|3|16.04|23.11|27|$ 6,495.81|11.89|💎 Champions / VIP|🥇 Very High|Exclusive offers, loyalty rewards.|Email, VIP newsletters, App push.|
#

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
**Heatmap - Customer Segmentation Count Using RFM Analysis**
![Heatmap - Customer Segmentation Count Using RFM Analysis](../5_Prescriptive_Sales_Analysis/Assets/Py_20_Customer_Segmentation_Count_Using_RFM%20Analysis_Heatmap.png)  
*Generated using seaborn library*
#
**Countplot - Customer Segmentation Count Using RFM Analysis**
![Countplot - Customer Segmentation Count Using RFM Analysis](../5_Prescriptive_Sales_Analysis/Assets/Py_21_Customer_Segmentation_Count_Using_RFM_Analysis_Countplot.png)  
*Generated using seaborn library*
#
**Scatterplot - Customer Segmentation Using RFM Analysis - Monetary Vs Segment**
![Scatterplot - Customer Segmentation Using RFM Analysis - Monetary Vs Segment](../5_Prescriptive_Sales_Analysis/Assets/Py_22_Customer_Segmentation_Using_RFM_Analysis_Monetary_Vs_Segment_Scatterplot.png)  
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
- **`Recency`**: **The number of days since last purchase**.
- **`Frequency`**: **The number of purchases**.
- **`Monetary`**: **The total revenue/profit generated**.
- **`R_Score`**: **Recency score**.
- **`F_Score`**: **Frequency score**.
- **`M_Score`**: **Monetary score**.
- **`RFM_Segment`**: **Recency + Frequency + Monetary score**.
- **`Cluster`**: **3**, **2**, **1** and **0**.
- **`predicted_cltv_6m`**: **The predicted CLTV for 6 months**.
- **`cltv_segment`**:	**"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**.
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
- **`cltv_segment`**:	**"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**.
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
 - **`Response Rate`**.
 - **`Cost Per Customer`**.
 - **`Expected Response`**.
 - **`Expected Revenue`**.
 - **`Total Cost`**.
 - **`Profit`**.
 - **`ROI %`**.

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

### Churn Prediction And Logistic Regression Model

#### What Is The Purpose Of Churn Prediction?

- Finds the **`75th`** or **`95th percentile`** of **`recency`**.

- Flags customers in the **`top 25%`** or **`top 5%`** of **`inactivity`** as **`churned`**.

- Offers flexibility — you can change to **`.quantile(0.80)`** for a more **`aggressive threshold`**.

 
### Key Metrics Evaluated
1) Top 10 Customers By CLTV-Days.
2) Top 10 Customers By CLTV-Months.
3) Strategic Insights: Correlation Analysis Of Key Metrics.
4) Recency Distribution.
5) Churn Threshold.
6) Top 5 Active Customers.
7) Top 5 Churned Customers.

### 🏗️ Auto-calculated churn threshold (95th percentile)

#
```python

# Auto-calculate churn threshold (e.g., 95th percentile)
auto_churn_threshold = customer_features['recency'].quantile(0.95)

#==#

# Step 9: Apply churn rule
customer_features['churn_status'] = np.where(customer_features['recency'] > auto_churn_threshold, 1, 0) # 0 = Active, 1 = Churned

#==#

# Step 10: Summary
print("Reference date:", reference_date.date())
# print(f"Auto-calculated churn threshold (75th percentile): {int(auto_churn_threshold)} days")
print(f"\nAuto-calculated churn threshold (95th percentile): {int(auto_churn_threshold)} days")
print(f'\n{customer_features['churn_status'].value_counts().round(2)}')
print(f'\n{customer_features['churn_status'].value_counts(normalize=True).rename({0:'Active', 1:'Churned'}).round(2)}')

```
#

### 🖼️ Results Snapshot

#
```python
Reference date: 2023-10-02

Auto-calculated churn threshold (95th percentile): 63 days

churn_status
0    157
1      9
Name: count, dtype: int64

churn_status
Active     0.95
Churned    0.05

```

### **🔍 Insights**
- The churn threshold (95th percentile) is **`63 days`**.

#

### Dataframe Columns
- **`customer_reference_id`**: **The customer ID**.
- **`cltv_days`**: **The pedicted total revenue/profit generated over the period of the relationship in days (Short-term campaigns, daily churn modelling..)**.
- **`cltv_months`**: **The pedicted total revenue/profit generated over the period of the relationship in months (Business forecasting and marketing budgets)**.
- **`monetary`**: **The total revenue/profit generated**.
- **`avg_order_value`**: **The mean amount spent on an order**.
- **`first_purchase`**: **The first purchase**.
- **`last_purchase`**: **The last purchase**.
- **`recency`**: **The number of days since last purchase**.
- **`frequency`**: **The number of purchases**.
- **`customer_lifespan_days`**: **The period of time in days the customer has been continuously ordering**.
- **`purchase_freq_daily`**: **The average number of orders placed per day**.
- **`cltv_tier_days`**: **"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**.
- **`cltv_tier_months`**: **"Very High"**, **"High"**, **"Medium"**, **"Low"** and **"Very Low"**.
- **`customer_value`**: 
  - **"VIP Revenue Drivers"**.
  - **"High Value Customers"**.
  - **"Growth Opportunity Customers"**.
  - **"Low Value Customers"**.
  - **"Dormant or At-Risk"**.
- **`recommended_strategy`**: 
  - **"Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service"**.
  - **"Upsell premium products, cross-sell related items, reward referrals"**.
  - **"Educate on product benefits, send tailored content and offers to increase engagement"**.
  - **"Encourage repeat purchases with discounts or bundle deals, explore churn reasons"**.
  - **"Re-engagement campaigns, win-back emails, limited-time incentives, or exit surveys"**.
- **`suggested_channels`**:
  - **"Email, SMS, Personalised landing"**.
  - **"Email, Paid Ads, Mobile App"**.
  - **"Email Series, Blog, Social Media"**.
  - **"Email, Push Notification"**.
  - **"Email, Re-targeting Ads"**.
- **`frequency`**:
  - **"Weekly"**.
  - **"Bi-weekly"**.
  - **"Weekly"**.
  - **"Monthly"**.
  - **"Immediate"**.
- **`churn_status`**: **Active** and **Churned** .

### **🩺 Diagnostics**
  - Dataframes.
  - Heatmap.
  - Histplot.
  
### 🖼️ Results Snapshot

#
**Top 10 Customers By CLTV-Days**
|customer_id|cltv_days|avg_order_value|total_orders|customer_lifespan_days|purchase_freq_daily|cltv_tier_days|customer_value|recommended_strategy|suggested_channels|frequency|
|-------|-------|---------|--------------|--------|---------|---------------|--------------|--------------------|------|----|
|4040|$ 10,363.0|416.0|25 |346|0.072|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|
|4109|$ 10,021.0|626.0|16|348|0.046|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|
|4044|$ 9,321.0|388.0|24|312|0.077|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|        
|4108|$ 7,671.0|296.0|26|365|0.071|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|        
|4075|$ 7,651.0|274.0|28|358|0.078|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|        
|4010|$ 7028.0|292.0|24|339|0.071|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|      
|3984|$ 6,912.0|362.0|19|285|0.067|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|      
|4103|$ 6,733.0|293.0|23|343|0.067|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|    
|4002|$ 6,708.0|258.0|26|321|0.081|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|       
|4067|$ 6,703.0|318.0|21|310|0.068|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|
#

### **🔍 Insights**
 - **TBC**.
  
#
**Top 10 Customers By CLTV-Months**
|customer_id|cltv_months|avg_order_value|total_orders|customer_lifespan_months|purchase_freq_monthly|cltv_tier_months|customer_value|recommended_strategy|suggested_channels|frequency|
|-------|-------|---------|--------------|--------|---------|---------------|--------------|--------------------|------|----|
|4040|$ 10,833.0|416.0|25 |12.0|2.17|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|
|4109|$ 10,367.0|626.0|16|12.0|1.38|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|
|4044|$ 8,963.0|388.0|24|10.0|2.31|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|        
|4075|$ 7,727.0|274.0|28|12.0|2.35|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|        
|4108|$ 7,601.0|296.0|26|12.0|2.14|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|        
|3984|$ 7240.0|362.0|19|10.0|2.00|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|      
|4002|$ 6,896.0|258.0|26|11.0|2.43|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|      
|4010|$ 6,809.0|292.0|24|11.0|2.12|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|    
|3986|$ 6,677.0|281.0|23|12.0|1.98|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|       
|4103|$ 6,478.0|293.0|23|11.0|2.01|Very High|VIP Revenue Drivers|Prioritise with exclusive perks, early access to launches, loyalty programs, and 1:1 service|Email, SMS, Personalised landing|Weekly|                                                                                                             
#

### **🔍 Insights**
 - **TBC**.

#

### 📷 Visualisation

#
**Barplot - Top 10 Customers By CLTV-Days**
![Barplot - Top 10 Customers By CLTV-Days](../5_Prescriptive_Sales_Analysis/Assets/Py_23_Top_10_Customers_By_CLTV_Days_Barplot.png)  
*Generated using seaborn library*
#
**Barplot - Top 10 Customers By CLTV-Months**
![Barplot - Top 10 Customers By CLTV-Months](../5_Prescriptive_Sales_Analysis/Assets/Py_24_Top_10_Customers_By_CLTV_Months_Barplot.png)   
*Generated using seaborn library*
#
**Heatmap - Strategic Insights: Correlation Analysis Of Key Metrics**
![Heatmap - Strategic Insights: Correlation Analysis Of Key Metrics](../5_Prescriptive_Sales_Analysis/Assets/Py_38_Strategic_Insights_Correlation_Analysis_Of_Key_Metrics_Heatmap.png)   
*Generated using seaborn library*
#
**Histplot - Recency Distribution**
![Histplot - Recency Distribution](../5_Prescriptive_Sales_Analysis/Assets/Py_39_Recency_Distribution_Histplot.png)   
*Generated using seaborn library*
#
**Dataframe - Top 5 Active Customers**
![Dataframe - Top 5 Active Customers](../5_Prescriptive_Sales_Analysis/Assets/Py_40_Top_5_Active_Customers.png)   
*Generated using pandas library*
#
**Dataframe - Top 5 Churned Customers**
![Dataframe - Top 5 Churned Customers](../5_Prescriptive_Sales_Analysis/Assets/Py_41_Top_5_Inactive_Customers.png)   
*Generated using pandas library*
#

### **🔍 Insights**
 - **TBC**.

#

### 🏗️ Logistic Regression Model

#
```python

# Prepare Features for Modeling - Logistic Regression Model

# Drop any non-numeric or ID columns that shouldn't be part of training
X = customer_features[['customer_reference_id', 'cltv_days', 'avg_order_value', 
                       'monetary', 'recency', 'frequency',  
                       'customer_lifespan_days', 'purchase_freq_daily']] # You can expand to include RFM, CLTV, etc.
y = customer_features['churn_status']

#==#

# Train-Test Split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42, stratify=y)
print (f'Training data (70%)|(# Obs, # Cols): \t{X_train.shape, y_train.shape}') # Seen data. Observations, Number of columns.
print (f'Test data (30%)|(# Obs, # Cols):  \t{X_test.shape, y_test.shape}') # Unseen data. Observations, Number of columns.

#==#

# Build and Train Logistic Regression Model

# Instantiate the model
logreg_model = LogisticRegression(max_iter=1000)
# Reasons for using this model:
# Increases the maximum number of iterations (default is 100). 
# Good for large or complex datasets where the model needs more iterations to find the best solution.

# Fit the model with data
logreg_model.fit(X_train, y_train)

#==#

# Build and Train Logistic Regression Model (Random Seed)

# # Instantiate the model
# logreg_model = LogisticRegression(random_state=16) 
# # Reasons for using this model:
# # Sets the random seed for reproducibility. 
# # Good for ensuring your results are reproducible (e.g., in experiments or production code).

# # # Fit the model with data
# logreg_model.fit(X_train, y_train)

#==#

# Evaluate Model
# Predictions
y_pred = logreg_model.predict(X_test)
y_proba = logreg_model.predict_proba(X_test)[:, 1]

#==#

# Confusion matrix
print(f'Confusion Matrix:\n{confusion_matrix(y_test, y_pred)}')

# Classification Report
print(f'Classification Report:{classification_report(y_test, y_pred)}')

# ROC-AUC Score
print(f'ROC-AUC Score: {roc_auc_score(y_test, y_proba):.2%}')

```
#

### 🖼️ Results Snapshot

#
```python

Training data (70%)|(# Obs, # Cols): 	((116, 8), (116,))
Test data (30%)|(# Obs, # Cols):  	((50, 8), (50,))
Confusion Matrix:
[[46  1]
 [ 0  3]]
Classification Report:              precision    recall  f1-score   support

           0       1.00      0.98      0.99        47
           1       0.75      1.00      0.86         3

    accuracy                           0.98        50
   macro avg       0.88      0.99      0.92        50
weighted avg       0.98      0.98      0.98        50

ROC-AUC Score: 100.00%

```
#

### **🔍 Insights**

**`Confusion Matrix:`**
- **You have two classes `0` and `1`.** 

- **`Diagonal values` represent `accurate predictions`, while `non-diagonal elements` are `inaccurate predictions`.** 

- **In the output, `46` and `3` are `actual predictions`, and `0` and `1` are `incorrect predictions`.**

**`Classification Report:`**

- **`Accuracy`: We have a classification report accuracy of `100%`. The model has excellent prediction accuracy.**

- **`Precision`: We have a classification report precision score of `100%`. The model has excellent prediction precision.**

- **`Recall`: We have a classification report recall score of `100%`. The model is able to identify `0:Active` & `1:churned` in our test set `100%` of the time .**

#

### 📷 Visualisation

#
**Lineplot - ROC Curve - Logistic Regressions**
![Lineplot - ROC Curve - Logistic Regression](../5_Prescriptive_Sales_Analysis/Assets/Py_43_ROC_Curve_Logistic_Regression_Linelot.png)  
*Generated using seaborn library*
#

### **🔍 Insights**

**`Area Under the Receiver Operating Characteristic Curve (AUC-ROC)`**:

- The model scored an AUC-ROC score of **`100%`**!.

- **`AUC-ROC`** **`measures how well`** the **`predicted probabilities distinguish between two classes`** e.g `(positive/negative, disease/no disease)`. In our case **`0:Active`** & **`1:churned`**.

- A **`higher AUC means a better model at distinguishing between classes`**.

- **`The area under the ROC curve (AUC) is a single value that summarises the overall performance of the model`**.

- An AUC of **`1`** represents a **`perfect classifier`**, while an AUC of **`0.5`** indicates **`random guessing`**.

**`AUC-ROC Scoring Overview`**:

![alt text](<Screenshot 2025-09-09 105557.png>)

#

### (A/B), (A/B/C) And (A/B/C/D) Testing

#### What Is A/B Testing?
- A/B testing—also called **`split testing`** or **`bucket testing`**—compares the **`performance`** of **`two versions of content`** to see which one **`appeals more`** to visitors/viewers.

- It **`tests`** a **`control (A) version`** against a **`variant (B) version`** to **`measure`** which one is **`most successful`** based on your **`key metrics`**.

#### Why is it important?
- A/B testing helps you **`determine how to provide the best customer experience (CX)`**.

- It plays an **`important`** role in **`campaign management`** since it helps **`determine`** what **`is`** and **`isn’t working`**.

- It shows what your **`audience`** is **`interested`** in and **`responds`** to.

- It can help you see which element of your **`marketing strategy`** has the **`biggest impact`**, which one **`needs improvement`**, and which one **`needs to be dropped`** altogether.

### Key Metrics Evaluated
1) A/B Test Simulation: Based On Existing Features.
2) A/B Test Simulation: Response Rate (%) Comparison.
3) A/B Test: Measuring Incremental Impact Of Marketing Treatment On Customer Response.
4) A/B Test - Uplift (%)  By CLTV Tier And Churn Status.

### **🩺 Diagnostics**
  - Dataframes.
  - Barplots.
  - Heatmap.

### 📷 Visualisation

#
**Dataframe - A/B Test Simulation: Based On Existing Features**
![Dataframe - A/B Test Simulation (Based On Existing Features)](../5_Prescriptive_Sales_Analysis/Assets/Py_44_A_B_Test_Simulation_Based_On_Existing_Features.png)  
*Generated using pandas library*
#
**Dataframe - A/B Test Simulation: Response Rate (%) Comparison**
![Dataframe - A/B Test Simulation: Response Rate (%) Comparison](../5_Prescriptive_Sales_Analysis/Assets/Py_45_Simulated_AB_Test_Response_Rate_(%25)_Comparison.png)   
*Generated using pandas library*
#
**Barplot - A/B Test Simulation: Response Rate (%) Comparison**
![Barplot - A/B Test Simulation: Response Rate (%) Comparison](../5_Prescriptive_Sales_Analysis/Assets/Py_46_AB_Test_Simulation_Response_Rate_Comparison_Barplot.png)   
*Generated using seaborn library*
#
**Dataframe - A/B Test: Measuring Incremental Impact Of Marketing Treatment On Customer Response**
![Dataframe - A/B Test: Measuring Incremental Impact Of Marketing Treatment On Customer Response](../5_Prescriptive_Sales_Analysis/Assets/Py_47_AB_Test_Measuring_Incremental_Impact_Of_Marketing_Treatment_On_Customer_Response.png)  
*Generated using pandas library*
#
**Barplot - A/B Test: Measuring Incremental Impact Of Marketing Treatment On Customer Response**
![Barplot - A/B Test: Measuring Incremental Impact Of Marketing Treatment On Customer Response](../5_Prescriptive_Sales_Analysis/Assets/Py_48_AB_Test_Measuring_Incremental_Impact_Of_Marketing_Treatment_On_Customer_Response_Barplot.png)  
*Generated using seaborn library*
#
**Dataframe - A/B Test - Uplift (%)  By CLTV Tier And Churn Status**
![Dataframe - A/B Test - Uplift (%)  By CLTV Tier And Churn Status](../5_Prescriptive_Sales_Analysis/Assets/Py_49_AB_Test_Uplift_(%25)_By_CLTV_Tier_And_Churn_Status.png)  
*Generated using pandas library*
#
**Barplot - A/B Test - Uplift (%)  By CLTV Tier And Churn Status**
![Barplot - A/B Test - Uplift (%)  By CLTV Tier And Churn Status](../5_Prescriptive_Sales_Analysis/Assets/Py_50_A_B_Test_Uplift_Percentage_By_CLTV_Tier_Days_And_Churn_Status_Barplot.png)  
*Generated using seaborn library*
#
**Heatmap - A/B Test - Uplift (%)  By CLTV Tier And Churn Status**
![Heatmap - A/B Test - Uplift (%)  By CLTV Tier And Churn Status](../5_Prescriptive_Sales_Analysis/Assets/Py_51_AB_Test_Uplift_Percentage_By_CLTV_Tier_Days_And_Churn_Status_Heatmap.png)  
*Generated using seaborn library*
#

### **🔍 Insights**
 - **TBC**.

#

### A/B Test - Qini Curve

#### What Is The Qini Curve?
- A Qini curve is a **`visualisation tool`** used in **`uplift modeling`** to **`assess the effectiveness of treatment targeting strategies`**.

- It plots the **`cumulative gain (or uplift)`** achieved by **`targeting a certain percentage of the population`**, compared to **`random targeting`**.

#### Why is it important?
- This helps in **`understanding how well a model can identify individuals`** who will **`respond positively`** to a treatment, allowing for **`more efficient resource allocation`**.

  - Imagine you have a marketing campaign and want to know which customers are most likely to respond to it.
  - A Qini curve helps you **`visualise how well your targeting strategy (e.g., using a machine learning model) performs`** compared to **`simply picking customers at random`**.

- **`Example Of A Qini Curve`**:

![alt text](<Screenshot 2025-06-30 113838.png>)

#### How It Works?
**1. `Uplift Modeling`**:
- Uplift modeling aims to identify the **`"persuadables"`** – individuals whose **`behavior`** is **`most likely to be influenced`** by a **`treatment`** (`like a marketing campaign`).

**2. `Ranking Customers`**:
- A model predicts the **`"uplift score"`** for each customer, which represents the **`likelihood of a positive response due to the treatment`**.

**3. `Creating the Curve`**:
- The Qini curve plots the **`cumulative gain (e.g., extra conversions)`** achieved by **`targeting the top N% of customers based on their uplift scores`**, against the **`percentage of the population targeted`**.

**4. `Interpreting the Curve`**:
- A **`steeper curve at the beginning`** indicates a **`better targeting strategy`**, meaning the **`model is effectively identifying`** individuals who **`will respond well`** to the treatment early on.

**5. `Comparing Models`**:
- The Qini curve can be used to **`compare the performance of different uplift models`** *or* **`targeting strategies`**.

**`Key Concepts`**:
- **`Uplift`**: **The incremental impact of a treatment on an individual**.
- **`Targeting`**: **Selecting specific individuals for treatment based on their uplift scores**.
- **`Gain`**: **The benefit or positive outcome achieved by the treatment**.

### **🩺 Diagnostics**
  - Lineplot.

### 📷 Visualisation

#
**Lineplot - A/B Test - Qini Curve: Incremental Impact Vs Random**
![Lineplot - A/B Test - Qini Curve: Incremental Impact Vs Random](../5_Prescriptive_Sales_Analysis/Assets/Py_52_AB_Test_Qini%20Curve_Incremental_Impact_Vs_Random_Line_Plot.png)  
*Generated using seaborn library*
#

### **🔍 Insights**
- The **`more the blue curve rises above the dashed line`**, the **`better your (future) uplift model at picking customers who truly benefit`**.

- If you see **`strong early lift`**, you can **`reduce campaign size`** and **`still capture most of the incremental responses`**.

#

### (A/B/C/D) Testing

#### What Is A/B/C/D Testing?
- A/B/C/D testing, also known as **`multivariate testing`**, is a method used to compare **`multiple versions`** of a webpage, email, or other content to **`see which performs best`**.

- It is an **`extension of A/B testing`**, which **`compares only two versions (A and B)`**.

#### Why is it important?
- In A/B/C/D testing, **`several variations`** **`(A, B, C, and potentially D)`** are **`tested simultaneously`** to **`identify the most effective one`**.

### Key Metrics Evaluated
1) A/B/C/D Test - Calculating Response Rates (%) By Campaigns And Uplift (%) Vs Control.

### **🩺 Diagnostics**
  - Dataframe.
  - Barplot.

### 📷 Visualisation

#
**Dataframe - A/B/C/D Test - Calculating Response Rates (%) By Campaigns And Uplift (%) Vs Control**
![Dataframe - A/B/C/D Test - Calculating Response Rates (%) By Campaigns And Uplift (%) Vs Control](../5_Prescriptive_Sales_Analysis/Assets/Py_53_ABCD_Test_Calculating_Response_Rates_(%25)_By_Campaigns_And_Uplift_(%25)_Vs_Control.png)  
*Generated using pandas library*
#
**Barplot - A/B/C/D Test - Uplift (%) Vs Control By Campaign**
![Barplot - A/B/C/D Test - Uplift (%) Vs Control By Campaign](../5_Prescriptive_Sales_Analysis/Assets/Py_54_ABCD_Test_Uplift_Percentage_Vs_Control_By_Campaign_Barplot.png)   
*Generated using seaborn library*
#

### **🔍 Insights**
 - **TBC**.

#

### (A/B/C) Testing

#### What Is A/B/C Testing?
- A/B/C testing is an experiment where you **`compare three or more versions`** of something to **`determine which performs best`**. 

- It is an **`extension of A/B testing`**, which **`compares only two versions`**.

#### Why is it important?
- A/B/C testing is useful for **`comparing a control group against multiple variations`** to see which **`drives the best results`**.

### Key Metrics Evaluated
1) A/B/C Test - Qini Curve Per Campaign With ROI Benchmarks (Randon Assignment Version).
2) A/B/C Test - Qini Curve Per Campaign — Simulated Response By Personalised Score With ROI Benchmarks (CLTV-Tiered Assignment Version).

### **🩺 Diagnostics**
  - Lineplots.
 
### 📷 Visualisation

#
**Lineplot - A/B/C Test - Qini Curve Per Campaign With ROI Benchmarks (Randon Assignment Version)**
![Lineplot - A/B/C Test - Qini Curve Per Campaign With ROI Benchmarks (Randon Assignment Version)](../5_Prescriptive_Sales_Analysis/Assets/Py_55_ABC_Test_Qini_Curve_Per_Campaign_With_ROI_Benchmarks_Random_Assignment_Version_Line_Plot.png)  
*Generated using seaborn library*
#
**Lineplot - A/B/C Test - Qini Curve Per Campaign — Simulated Response By Personalised Score With ROI Benchmarks (CLTV-Tiered Assignment Version)**
![Lineplot - A/B/C Test - Qini Curve Per Campaign — Simulated Response By Personalised Score With ROI Benchmarks (CLTV-Tiered Assignment Version)](../5_Prescriptive_Sales_Analysis/Assets/Py_56_ABC_Test_Qini_Curve_Per_Campaign_SR_By_PS_With_ROI_Benchmarks_Random_CLTV_Tiered_Asmt_Version_Line_Plot.png)   
*Generated using seaborn library*
#

### **🔍 Insights**
 - **TBC**.

#

### 🎯 Final Thoughts
- **TBC**.

#

## 📬 Contact
*Built by [Arkyl Trulock](https://github.com/ArkylTrulock)*  
For collaborations or feedback: X@gmail.com

