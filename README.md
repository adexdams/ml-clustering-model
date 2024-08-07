# ml-clustering-model
The model segments customers into groups that would inform the company's actions by helping them better understand the behaviourand needs of different types of customers.

## **Introduction**


### **Problem Definition**

The task is to develop a customer personality analysis that would help the retail business understand its customers and help in modifying the product based on its target from different types of customer segments.



### **About the Data**

This dataset contains information on customer purchase behavior across various attributes, aiming to help data scientists and analysts understand the factors influencing purchase decisions. The dataset includes demographic information, purchasing habits, and other relevant features.

It was sourced from **Kaggle**: https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis



### **About the Features**

**People**
* **ID:** Customer's unique identifier
* **Year_Birth:** Customer's birth year
* **Education:** Customer's education level
* **Marital_Status:** Customer's marital status
* **Income:** Customer's yearly household income
* **Kidhome:** Number of children in customer's household
* **Teenhome:** Number of teenagers in customer's household
* **Dt_Customer:** Date of customer's enrollment with the company
* **Recency:** Number of days since customer's last purchase
* **Complain:** 1 if the customer complained in the last 2 years, 0 otherwise

**Products**
* **MntWines:** Amount spent on wine in last 2 years
* **MntFruits:** Amount spent on fruits in last 2 years
* **MntMeatProducts:** Amount spent on meat in last 2 years
* **MntFishProducts:** Amount spent on fish in last 2 years
* **MntSweetProducts:** Amount spent on sweets in last 2 years
* **MntGoldProds:** Amount spent on gold in last 2 years

**Promotion**
* **NumDealsPurchases:** Number of purchases made with a discount
* **AcceptedCmp1:** 1 if customer accepted the offer in the 1st campaign, 0 otherwise
* **AcceptedCmp2:** 1 if customer accepted the offer in the 2nd campaign, 0 otherwise
* **AcceptedCmp3:** 1 if customer accepted the offer in the 3rd campaign, 0 otherwise
* **AcceptedCmp4:** 1 if customer accepted the offer in the 4th campaign, 0 otherwise
* **AcceptedCmp5:** 1 if customer accepted the offer in the 5th campaign, 0 otherwise
* **Response:** 1 if the customer accepted the offer in the last campaign, 0 otherwise

**Place**
* **NumWebPurchases:** Number of purchases made through the company’s website
* **NumCatalogPurchases:** Number of purchases made using a catalog
* **NumStorePurchases:** Number of purchases made directly in stores
* **NumWebVisitsMonth:** Number of visits to the company’s website in the last month

**Target**
* Need to perform clustering to summarize customer segments.


## Approach
1. Loaded the dataset and the necessary technologies
2. Sought the columns with empty values and filled them with the mean values
3. Checked for outlier numbers, found to be in the Annual Income column, and dropped the overly extreme numbers compared to the rest.
4. Worked on feature engineering activities by converting the year columns into datetime64.
5. In feature engineering, I also created a new column and calculated the age of each customer in the dataset.
6. Preprocessed the categorical and numerical dataset
7. Developed two models, KMeans and Gaussian Mixture models to cluster the datasets into 3 sections.
8. Scored the two models and ended up selecting the KMeans model instead (see conclusion for the dataset score).


## Conclusion

The KMeans model produced a marginally better silhouette score of 0.40 against the Gaussian Mixture which produced 0.39
