# samsung_sales_prediction_ML_oop
This is a Machine learning prediction for global samsung sales project

## Reports and Findings

The task of this dataset is to find the relationship between the features and the target revenue. 

This will help the company to determine the sales strategy and how to increase the revenue.  


The dataset is prepared as the following steps:
1. Data checking and cleaning
2. Statistical analysis
3. Encoding
4. Machine Learning model training

The dataset: 
The data sourced from year 2021 to 2024. 

The dataset contains 15500 row of entries. After exploring the data and cleaning, the final shape of the data for ML model is 27 features  and 15500 rows.

The distribution of the target variable, revenue is stated as follow: 

Revenue statistics:
count    15500.000000
mean      1478.145734
std       2368.688098
min          6.610000
25%        254.265000
50%        739.380000
75%       1695.315000
max      47665.900000



![revenue_distribution](revenue_dist)

The revenue is transformed into log form for better ML model prediction. 




We have found the highest number of units sold across each contry for all items:
	
country	units_sold
Norway	  834
India	    818
Sri Lanka	797
Canada	  788
UAE	      765
Indonesia	760
Greece	  745
Spain	    738
Austria	  733

![units sold](sales_count)










