# **Customer-Segmentation**

# Use Case

- Use Case Summary
- Objective Statement:
  * Get business insight about how many product sold every month.
  * Get business insight about how much customer spend their money every month.
  * To reduce risk in deciding where, when, how, and to whom a product, service, or brand will be marketed.
  * To increase marketing efficiency by directing effort specifically toward the designated segment in a manner consistent with that segment’s characteristics.

- Challenges:
  * Large size of data, can not maintain by excel spreadsheet.
  * Need several coordination from each department.
  * Demography data have a lot missing values and typo.

- Methodology / Analytic Technique:
  * Descriptive analysis
  * Graph analysis
  * Segment Analysis

- Business Benefit:
  * Helping Business Development Team to create product differentiation based on the characteristic for each customer.
  * Know how to treat customer with specific criteria.

- Expected Outcome:
  * Know how many product sold every month.
  * Know how much customer spend their money every month.
  * Customer segmentation analysis.
  * Recommendation based on customer segmentation.
  
# Business Understanding

- Retail is the process of selling consumer goods or services to customers through multiple channels of distribution to earn a profit.- This case has some business question using the data:
- How many product sold every month?
- How much customer spend their money every month?
- How about Customer segmentation analysis?
- How about recommendation based on customer segmentation?

# Data Understanding

- Data of Retail Transaction from 01 December 2010 to 09 December 2011
- Source Data: Online retail dataset by UCI Machine Learning Library. 
https://archive.ics.uci.edu/ml/datasets/Online+Retail
- Data Dictionary:
- InvoiceNo: Invoice number uniquely assigned to each transaction. 
- StockCode: Product (item) code.
- Description: Product (item) name.
- Quantity: The quantities of each product (item) per transaction. 
- InvoiceDate: The day and time when each transaction was generated.
- UnitPrice: Product price per unit in sterling.
- CustomerID: Customer number uniquely assigned to each customer.
- Country: The name of the country where each customer resides.

# Data preparation 

- Code Used:
- Python Version: 3.7.6
- Packages: Pandas, Numpy, Matplotlib, Seaborn, Sklearn, and Feature Engine 

# Data Cleansing 

- There are about 25% of Null CustomerID in the data. We need to remove them as there is no way we can get the number of CustomerID.
- There are few records with UnitPrice<0 and Quantity<0. We need to remove them from the analysis. This could represent cancelled or returned orders.
- There is more than 90% of 'United Kingdom' customers, therefore we will restrict the data to only United Kingdom customers.

# Exploratory Data Analysis

- How many product sold every month?
![count 1](https://user-images.githubusercontent.com/75175081/127734116-ed109eb3-686d-435d-96fd-d29255377ea6.png)
Product sold in November has highest quantity that has around 13,41% product sold from all transaction along 1 year. Therefore the business team can increase sales in this month such as promoting new products to customers in this month.

- How much customer spend their money every month?
![revenue 1](https://user-images.githubusercontent.com/75175081/127734242-42991f19-1ef5-4af5-b623-fdaf7c6cc122.png)
Revenue in November has highest amount that has  13,41% revenue from total revenue along 1 year. Therefore the business team can replicate the success of sales strategies in November to be implemented in other months

# RFM Analysis

- Recency Frequency Monetary (RFM)
- RFM analysis allows you to segment customers by the frequency and value of purchases and identify those customers who spend the most money.
- Recency — how long it’s been since a customer bought something from us.
- Frequency — how often a customer buys from us.
- Monetary value — the total value of purchases a customer has made.

# Modeling Data: RFM Quantiles

- Now we split the metrics into segments using quantiles.
- We will assign a score from 1 to 4 to each Recency, Frequency and Monetary respectively.
- 1 is the highest value, and 4 is the lowest value.
- A final RFM score (Overall Value) is calculated simply by combining individual RFM score numbers.

![image](https://user-images.githubusercontent.com/75175081/127734694-d312d392-7994-4f7d-adfe-e55d01fdc5f4.png)
![segmen rfm 1](https://user-images.githubusercontent.com/75175081/127734937-38b5fdbb-98c1-42e5-82c8-09da91023b33.png)

# Modeling Data: K-Means Clustering
- K-Means clustering algorithm is an unsupervised machine learning algorithm that uses multiple iterations to segment the unlabeled data points into K different clusters in a way such that each data point belongs to only a single group that has similar properties.
- K-means gives the best result under the following conditions:
- Data’s distribution is not skewed.
- Data is standardised.
- The data is highly skewed, therefore I will perform log transformations to reduce the skewness of each variable and I standardised the data.







