# samsung_sales_prediction_ML_oop
This is a Machine learning prediction for global samsung sales project

## Reports and Findings

### Dataset 
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

|Revenue | statistics |
|--------|------------|
|count  |  15500.000000|
|mean    |  1478.145734|
|std     |  2368.688098|
|min     |     6.610000|
|25%    |    254.265000|
|50%    |    739.380000|
|75%    |   1695.315000|
|max    |  47665.900000|



![revenue_distribution](img\revenue_dist)

The revenue is transformed into log form for better ML model prediction. 




We have found the highest number of units sold across each country for all items:

(selected data)

|country|	units_sold|
|--------|----------|
|Norway	 | 834|
|India	  |  818|
|Sri Lanka	|797|
|Canada	  |788|
|UAE	|      765|
|Indonesia	|760|
|Greece	 | 745|
|Spain	 |   738|
|Austria	|  733|

![units sold](img\sales_count)


We have also find out the correlation with the revenue and remove highly correlated features: 

![correlations](img\feature_corr)


### ML models

By using OOP, we can easily select the ML models we want. 

The ML models used in this data set are Linear regression and Random forest regression prediction.

#### Linear Regression


Training set:(12400, 27)  
Test set: (3100, 27)  

Model performance:  

Training set:  
R2 score: 0.9088 
MAE: $0.14  

Test set:  
R2 score: 0.9020  
MAE: $0.14  

Accuracy:  0.9020100073990232  



We have also foud out the top important coefficients for linear regressions: 

 TOP 10 Positive coefficeints (Increase Revenue)
 
 | Feature | Coefficient|
|-----------------------|------------|			 
 |    category_Monitor   |  0.272674 |
 | category_Appliances   |  0.272595 |
 |   category_Smart TV   |  0.264512 |
  |category_Galaxy Tab   |  0.247098 |
  |          is_5g_Yes   |  0.236500 |
  |         units_sold   |  0.141722 |
  |  category_Galaxy S   |  0.126653 |
  |  category_Galaxy Z   |  0.123760 |
|category_Galaxy Watch   |  0.029654 |
 |      color_Lavender   |  0.009932 |


 TOP 10 Negative coefficeints (Not help Revenue)



  | Feature | Coefficient|
|----------------------|---------------|
| color_Awesome Peach  |  -0.000839 |
 |       discount_pct  |  -0.002330 |
 |        color_Black  |  -0.003042 |
 |     region_Oceania  |  -0.003884 |
 |  color_Pink_violet  |  -0.004698 |
 |         color_Blue  |  -0.011573 |
 |  category_Galaxy A  |  -0.141940 |
|category_Galaxy Buds  |  -0.193492 |
|   category_Galaxy M  |  -0.264251 |
|category_Accessories  |  -0.737263 |



![linear regression plot](img/lr_plot)



### Random Forest Regression


Training set:(12400, 26)  
Test set: (3100, 26)  
Model performance:    

Training set:  
R2 score: 0.9141  
MAE: $0.12  

Test set:  
R2 score: 0.8405  
MAE: $0.18  

Accuracy:  0.8405175561632818  



 TOP 10 MOST IMPORTANT FEATURES 

 
 | Feature | Importance|
 |---------------|---------------|
 |category_Accessories |  0.419268|
  |         units_sold  |  0.252561|
 |   category_Smart TV   | 0.056917|
|category_Galaxy Watch  |  0.044540|
| category_Galaxy Buds   | 0.041421|
 |   category_Galaxy M  |  0.039713|
|    category_Galaxy A  |  0.037819|
 |        discount_pct  |  0.023971|
 |           is_5g_Yes   | 0.022984|
 |   category_Galaxy S  |  0.007063|


![RF feature importance](rf_importan)


## Conclusion

We have successfully make a data analysis on the sales data. 






