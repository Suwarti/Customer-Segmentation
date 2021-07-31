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







