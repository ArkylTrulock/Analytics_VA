# Introduction.
🛍️Dive into the Fashion Retail Market.
#
🚀Python code for my fashion retail sales anaylsis? Check them out here!: 
#
1. **Descriptive Sales Analysis[.ipynb](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Descriptive_Sales_Analysis.ipynb)**
2. **Diagnostic Sales Analysis[.ipynb](../Fashion_Retail_Sales_Data_Analysis/3_Diagnostic_Sales_Analysis/Diagnostic_Sales_Analysis.ipynb)**
3. **Predictive Sales Analysis[.ipynb](../Fashion_Retail_Sales_Data_Analysis/4_Predictive_Sales_Analysis/Predictive_Sales_Analysis.ipynb)**
4. **Prescriptive Sales Analysis[.ipynb](../Fashion_Retail_Sales_Data_Analysis/5_Prescriptive_Sales_Analysis/Prescriptive_Sales_Analysis.ipynb)**

#

# Background.
**📊What is Data Analysis?**
#
Data analysis is the process of collecting, cleaning, and transforming data to obtain insights to help make better and informed decisions. In our ever-growing, data-driven world, this is a must for companies of all sizes to solve everyday business problems. Each company has its own team, processes, and tools for data analysis projects.

Before beginning a data analysis project, a good starting point is to have a business objective in mind and a clearly defined problem. 

*What questions do you want to answer❓* After all, 90% of analytics is asking the right questions! 

*What are you measuring and how are you measuring it❓* You must also determine the metrics to measure performance. 
#
**While there is no prescribed data analysis process, these are the typical steps to follow:**
- **🗃️Collect** - Collecting the right data and just enough data for the project’s questions or problems that we want to research.
- **🧼Clean** - Detecting and correcting missing or inaccurate records from a data set. Data analysts typically spend about 70-80% of their time cleaning data.
- **🧮Analyse** - Identifying issues and using analytics to determine the root causes of issues. Analysing trends, correlations, variations, and outliers to help us focus on answering the questions (and any questions or objections others might have). This is the step where data analysts spend about 20-30% of their time.
- **🖼️Visualise** - Interpreting the results. We think about, What did we learn from the results of our  analysis? Does the data answer our original questions? How?’ This involves graphically showing our results in a way the team and leadership can easily and concisely understand them.
#
**The questions i wanted to answer through my python code were:**

1. **🔬Descriptive Analytics - What is happening❓** This involves the manipulating of raw data from multiple sources to give a data analyst valuable insights into the past and a view of key metrics within a business.
2. **🩺Diagnostic Analytics - Why are trends and patterns happening❓** This takes the insights found from descriptive analytics and drills down to find the causes of specific problems.
3. **🗠Predictive Analytics - What is likely to happen in the future❓** It is about forecasting. This type of analytics uses historical data to make predictions about the future.
4. **🫧What should happen❓** Combines the insight from all previous data analysis to determine a course of action to take to address a problem or make a decision. It uses advanced tools and technologies, like machine learning, business rules, and algorithms. This makes prescriptive analytics sophisticated to implement and manage.
#
# 🧰Libraries/Tools I Used:
For my deep dive into the fashion retail sales, I harnessed the power of several key libraries/tools:

- **Pandas**: Data analysis and manipulation tool, built on top of the Python programming language.
- **Numpy (Numerical Python)**: Mathematical and scientific computing library for Python programming tasks.
- **Seaborn**: Python data visualisation library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
- **Sklearn**: Machine learning library for the Python programming language.
- **Statsmodels**: Python library that provides classes and functions for the estimation of many different statistical models, as well as for conducting statistical tests, and statistical data exploration.
- **Prophet**: Tool for producing high quality forecasts for time series data that has multiple seasonality with linear or non-linear growth..
- **Pmdarima**: A statistical library designed to fill the void in Python's time series analysis capabilities, including the equivalent of R's auto.arima function..
- **Networkx**: Python package for the creation, manipulation, and study of the structure, dynamics, and functions of complex networks..
- **Mlxtend (Machine Learning Extensions)**: Python library of useful tools for the day-to-day data science tasks.
- **Lifetimes**: Python library used to forecast the total revenue a business expects to generate from a single customer relationship over their entire lifespan.
- **Visual Studio Code**: My go-to for database management and executing python code.
- **Git & Github**: Essential for version control and sharing my python code and analysis, ensuring collaboration and project tracking.
#
# Step 1 - Descriptive Sales Analysis.
As mentioned earlier, we want to find out what is happening. Through the manipulation of raw data we are able to deliver insights into the past and view key metrics in within the fashion retail business
#
## 🏦Assets

### 1. 💰The Counts, Total Sales And Percentange Share By Payment Methods.

**Columns**: **`payment_method`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`total_sales` in `descending order`.**
#
![The Counts, Total Sales And Percentange Share By Payment Methods - Table](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_01_The_Counts_Total_Sales_And_Percentage_Share_By_Payment_Methods.png)
*Generated using pandas library*
#
![The Counts, Total Sales And Percentange Share By Payment Methods - Pie Chart](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_02_The_Counts_Total_Sales_And_Percentage_Share_By_Payment_Method_Pie_Chart.png)
*Generated using seaborn library*
#
### 2. 💰Top 10 Items Purchased By Counts, Total Sales And Percentage Share.

**Columns**: **`items_purchased`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`total_sales` in `descending order`.**
#
**Dataframe**
![Top 10 Items Purchased By Counts, Total Sales And Percentage Share - Dataframe](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_03_Top_10_Items_Purchased_By_Counts_Total_Sales_And_Percentage_Share.png)
*Generated using pandas library*
#
**Barplot 1**
![Top 10 Items Purchased By Counts, Total Sales And Percentage Share - Barplot 1](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_04A_Top_10_Items_Purchased_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Barplot 2**
![Top 10 Items Purchased By Counts, Total Sales And Percentage Share - Barplot 2](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_04B_Top_10_Items_Purchased_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Barplot 3**
![Top 10 Items Purchased By Counts And Total Sales (2022 Vs 2023) - Barplot 3](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_04C_Top_10_Items_Purchased_By_Counts_And_Total_Sales_2022_Vs_2023_Barplot.png)
*Generated using seaborn library*
#
### 3. 💰Bottom 10 Items Purchased By Counts, Total Sales And Percentage Share.
**Columns**: **`items_purchased`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`total_sales` in `descending order`.**
#
**Dataframe**
![Bottom 10 Items Purchased By Counts, Total Sales And Percentage Share - Dataframe](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_05_Bottom_10_Items_Purchased_By_Counts_Total_Sales_And_Percentage_Share.png)
*Generated using pandas library*
#
**Barplot 1**
![Bottom 10 Items Purchased By Counts, Total Sales And Percentage Share - Barplot 1](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_06A_Bottom_10_Items_Purchased_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Barplot 2**
![Bottom 10 Items Purchased By Counts, Total Sales And Percentage Share - Barplot 2](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_06B_Bottom_10_Items_Purchased_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Barplot 3**
![Bottom 10 Items Purchased By Counts And Total Sales (2022 Vs 2023) - Barplot 3](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_06C_Bottom_10_Items_Purchased_By_Counts_And_Total_Sales_2022_Vs_2023_Barplot.png)
*Generated using seaborn library*
#
### 4. 💰Top Review Ratings By Counts, Total Sales And Percentage Share.
**Columns**: **`review_rating`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`review_rating` in `ascending order`.**
#
**Dataframe**
![Top Review Ratings By Counts, Total Sales And Percentage Share - Dataframe](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_07_Top_Review_Ratings_By_Counts_Total_Sales_And_Percentage_Share.png)
*Generated using pandas library*
#
**Barplot 1**
![Top Review Ratings By Counts, Total Sales And Percentage Share - Barplot 1](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_08A_Top_Review_Ratings_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Barplot 2**
![Top Review Ratings By Counts, Total Sales And Percentage Share - Barplot 2](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_08B_Top_Review_Ratings_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Barplot 3**
![Top Review Ratings By Counts, Total Sales And Percentage Share - Barplot 3](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_08C_Top_Review_Ratings_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
### 5. 💰Top Days By Counts, Total Sales And Percentage Share.
**Columns**: **`day`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`day` in `ascending order`.**
#
**Dataframe**
![Top Days By Counts, Total Sales And Percentage Share - Dataframe](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_09_Top_Days_By_Counts_Tota_Sale_And_Percentage_Share.png)
*Generated using pandas library*
#
**Barplot**
![Top Days By Counts, Total Sales And Percentage Share - Barplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_10A_Top_Days_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Stripplot**
![Day Vs Total Sales - Stripplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_10B_Day_Vs_Total_Sales_Stripplot.png)
*Generated using seaborn library*
#
**Kdeplot**
![Density Of Total Sales Across Each Day - Kdeplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_10C_Density_Of_Total_Sales_Across_Each_Day_Kdeplot.png)
*Generated using seaborn library*
#
### 6. 💰Top Months By Counts, Total Sales And Percentage Share.
**Columns**: **`month`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`month` in `ascending order`.**
#
**Dataframe**
![Top Months By Counts, Total Sales And Percentage Share - Dataframe](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_11_Top_Months_By_Counts_Total_Sales_And_Percentage_Share.png)
*Generated using pandas library*
#
**Barplot**
![Top Months By Counts, Total Sales And Percentage Share - Barplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_12A_Top_Months_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Stripplot**
![Month Vs Total Sales - Stripplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_12B_Month_Vs_Total_Sales_Stripplot.png)
*Generated using seaborn library*
#
**Kdeplot**
![Density Of Total Sales Across Each Month - Kdeplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_12C_Density_Of_Total_Sales_Across_Each_Month_Kdeplot.png)
*Generated using seaborn library*
#
### 7. 💰Top Quarters By Counts, Total Sales And Percentage Share.
**Columns**: **`quarter`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`quarter` in `ascending order`.**
#
**Dataframe**
![Top Quarters By Counts, Total Sales And Percentage Share - Dataframe](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_13_Top_Quarters_By_Counts_Total_Sales_And_Percentage_Share.png)
*Generated using pandas library*
#
**Barplot**
![Top Quarters By Counts, Total Sales And Percentage Share - Barplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_14A_Top_Quarters_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Lineplot**
![Top Quarters By Counts, Total Sales And Percentage Share - Lineplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_14B_Top_Quarters_By_Counts_Total_Sales_And_Percentage_Share_Line_Plot.png)
*Generated using seaborn library*
#
**Stripplot**
![Quarter Vs Total Sales - Stripplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_14C_Quarter_Vs_Total_Sales_Stripplot.png)
*Generated using seaborn library*
#
**Kdeplot**
![Density Of Total Sales Across Each Quarter - Kdeplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_14D_Density_Of_Total_Sales_Across_Each_Quarter_Kdeplot.png)
*Generated using seaborn library*
#
### 8. 💰Top Quarter Labels By Counts, Total Sales And Percentage Share.
**Columns**: **`quarter_label`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`quarter_label` in `ascending order`.**
#
**Dataframe**
![Top Quarter Labels By Counts, Total Sales And Percentage Share - Dataframe](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_15_Top_Quarter_Labels_By_Counts_Total_Sales_And_Percentage_Share.png)
*Generated using pandas library*
#
**Barplot**
![Top Quarter Labels By Counts, Total Sales And Percentage Share - Barplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_16A_Top_Quarter_Labels_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Lineplot**
![Top Quarter Labels By Counts, Total Sales And Percentage Share - Lineplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_16B_Top_Quarter_Labels_By_Counts_Total_Sales_And_Percentage_Share_Line_Plot.png)
*Generated using seaborn library*
#
**Stripplot**
![Quarter Label Vs Total Sales - Stripplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_16C_Quarter_Label_Vs_Total_Sales_Stripplot.png)
*Generated using seaborn library*
#
**Kdeplot**
![Density Of Total Sales Across Each Quarter Label - Kdeplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_16D_Density_Of_Total_Sales_Across_Each_Quarter_Label_Kdeplot.png)
*Generated using seaborn library*
#
### 9. 💰Top Years By Counts, Total Sales And Percentage Share.
**Columns**: **`year`, `count`, `count_rank`, `pct_count`, `count_diff`, `count_pct_diff`, `avg_total_sales`, `total_sales`, `sales_rank`, `pct_total_sales`, `total_sales_diff` and `total_sales_pct_diff`.**

**Filter**: **`year` in `ascending order`.**
#
**Dataframe**
![Top Years By Counts, Total Sales And Percentage Share - Dataframe](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_17_Top_Years_By_Counts_Total_Sales_And_Percentage_Share.png)
*Generated using pandas library*
#
**Barplot**
![Top Years By Counts, Total Sales And Percentage Share - Barplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_18A_Top_Years_By_Counts_Total_Sales_And_Percentage_Share_Barplot.png)
*Generated using seaborn library*
#
**Lineplot**
![Top Years By Counts, Total Sales And Percentage Share - Lineplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_18B_Top_Years_By_Counts_Total_Sales_And_Percentage_Share_Line_Plot.png)
*Generated using seaborn library*
#
**Stripplot**
![Year Vs Total Sales - Stripplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_18C_Year_Vs_Total_Sales_Stripplot.png)
*Generated using seaborn library*
#
**Kdeplot**
![Density Of Total Sales Across Each Year - Kdeplot](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Py_18D_Density_Of_Total_Sales_Across_Each_Year_Kdeplot.png)
*Generated using seaborn library*
#
**Descriptive Sales Analysis Excel Overview[.xlsx](../Fashion_Retail_Sales_Data_Analysis/2_Descriptive_Sales_Analysis/Assets/Descriptive_Sales_Analysis_Excel.xlsx)**