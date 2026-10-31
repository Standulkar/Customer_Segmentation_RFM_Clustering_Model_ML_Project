# Customer_Segmentation_RFM_Clustering_Model_ML_Project
Customer Segmentation of Online Retail


**RFM Analysis | K-Means Clustering | Python | Exploratory Data Analysis**

## Project Overview

This project focuses on identifying meaningful customer segments based on purchasing behavior using **RFM (Recency, Frequency, Monetary) Analysis and K-Means Clustering**.

The analysis uses transactional data from a UK-based online retail company that primarily sells unique gifts, with many customers being wholesalers.

The objective is to group customers with similar purchasing patterns and provide actionable insights to support customer retention, personalized marketing, and business growth.

## Problem Statement

Businesses often struggle to understand customer purchasing behavior and identify their most valuable customers.

This project aims to:

- Identify distinct customer segments based on purchasing behavior.
- Analyze customer purchase recency, frequency, and spending.
- Identify high-value, potential loyal, and at-risk customers.
- Apply unsupervised machine learning for customer segmentation.
- Recommend targeted marketing strategies for different customer groups.

## Dataset Information

The project uses the **Online Retail Dataset**, containing transactions recorded between December 1, 2010, and December 9, 2011.

- **Initial Records:** 541,909
- **Total Features:** 8
- **Dataset Type:** Transactional retail data
- **Business Domain:** E-commerce / Retail

### Dataset Features

| Feature | Description |
|---|---|
| InvoiceNo | Unique invoice number |
| StockCode | Unique product code |
| Description | Product description |
| Quantity | Quantity purchased |
| InvoiceDate | Transaction date and time |
| UnitPrice | Price per unit (£) |
| CustomerID | Unique customer identifier |
| Country | Customer's country |

## Technologies and Libraries

**Programming Language:** Python

**Libraries:**
- Pandas – Data manipulation and analysis
- NumPy – Numerical operations
- Matplotlib – Data visualization
- Seaborn – Statistical visualization
- Scikit-learn – Machine learning and preprocessing
- Yellowbrick – Elbow method visualization

**Environment:** Jupyter Notebook / Google Colab

## Project Workflow

### 1. Data Cleaning and Preprocessing

Performed data preprocessing to improve data quality before customer segmentation.

Key operations:

- Identified and removed duplicate records.
- Handled missing values.
- Removed cancelled transactions.
- Excluded transactions with zero unit prices.
- Converted InvoiceDate into datetime format.
- Created a Total Amount feature using Quantity × UnitPrice.

After removing missing values and duplicates, approximately **401K records** remained. After excluding cancelled transactions, **392,732 records** remained before additional filtering.

### 2. Exploratory Data Analysis (EDA)

Performed EDA to understand sales trends and customer purchasing patterns.

Key analyses included:

- Top 5 most and least frequently appearing products.
- Countries with the highest and lowest transaction activity.
- Top 10 customers' transaction share.
- Distribution of Quantity, UnitPrice, and Total Amount.
- Purchases by day of the week.
- Monthly purchasing trends.
- Purchasing patterns by hour and time of day.

**Key Observations:**

- Identified 4,338 unique customers in the cleaned dataset.
- The top 10 customers contributed approximately 9% of transaction rows.
- Numerical variables showed strong right-skewed distributions.
- Afternoon was identified as the most active purchasing period.
- The United Kingdom represented the primary market for further segmentation.

### 3. RFM Analysis

RFM analysis was performed on customers from the United Kingdom.

**Recency (R):** Number of days since a customer's most recent purchase.

**Frequency (F):** Number of transaction records associated with a customer.

**Monetary (M):** Total amount spent by a customer.

RFM analysis helps understand customer engagement and purchasing behavior.

### 4. Feature Transformation and Scaling

The RFM features exhibited right-skewed distributions.

To prepare the dataset for clustering:

- Applied log transformation to reduce skewness.
- Reduced the influence of extreme values.
- Applied StandardScaler to standardize the transformed features.

These steps helped make the RFM features more suitable for distance-based clustering.

### 5. K-Means Clustering

Implemented the **K-Means Clustering algorithm** to identify customer segments based on RFM features.

The Elbow Method was used to determine an appropriate number of clusters.

**Optimal number of clusters selected: 3**

K-Means was then applied to group customers into three distinct segments.

### 6. Cluster Interpretation Using RFM

Quartile-based RFM scoring was used to support customer behavior analysis.

Each customer received separate Recency, Frequency, and Monetary scores, helping interpret the characteristics of each cluster.

## Results and Customer Segments

The model identified three customer segments.

| Metric | Cluster 0 | Cluster 1 | Cluster 2 |
|---|---|---|---|
| Average Recency | ~68 days | ~165 days | ~11 days |
| Average Frequency | ~69 records | ~15 records | ~259 records |
| Average Monetary | ~£1,200 | ~£286 | ~£5,933 |
| Segment | Potential Loyalists | At-Risk Customers | Champions |

*Values are approximate and based on the cluster interpretations documented in the notebook.*

### Cluster 0 – Potential Loyalists

Customers with moderate purchasing frequency, spending, and recency.

**Business Recommendation:** Encourage repeat purchases through personalized offers, product recommendations, and loyalty programs.

### Cluster 1 – At-Risk / Lapsed Customers

Customers with high recency, low purchase frequency, and low spending.

**Business Recommendation:** Implement reactivation campaigns, targeted discounts, and personalized communication to improve customer retention.

### Cluster 2 – Champions / Loyal Customers

Customers with recent purchases, high transaction activity, and high monetary value.

**Business Recommendation:** Retain these valuable customers through exclusive offers, VIP loyalty programs, early product access, and referral incentives.

## Key Business Insights

- Customer purchasing behavior varies significantly across segments.
- High-value customers contribute substantial revenue and should be prioritized for retention.
- Inactive customers can be targeted through re-engagement strategies.
- Potential loyal customers present opportunities for increased engagement and spending.
- RFM-based clustering provides a practical foundation for customer-focused marketing strategies.

## How to Run the Project

1. Clone or download this GitHub repository.
2. Install the required Python libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn yellowbrick
   ```

3. Download the Online Retail dataset.
4. Open `Customer_Segmentation_ML_Model.ipynb` in Jupyter Notebook or Google Colab.
5. Update the dataset file path in the notebook to match your local environment.
6. Run the notebook cells sequentially to reproduce the analysis and clustering.

## Future Improvements

- Evaluate clustering quality using Silhouette Score.
- Compare K-Means with hierarchical clustering and DBSCAN.
- Build interactive dashboards using Power BI or Streamlit.
- Analyze customer lifetime value.
- Develop more advanced customer retention strategies.
- Explore how returns and cancellations affect net customer spending.

## Conclusion

This project demonstrates how **unsupervised machine learning and RFM analysis** can be used to understand customer purchasing behavior and identify meaningful customer segments.

Using K-Means clustering, customers were grouped into three segments: Potential Loyalists, At-Risk Customers, and Champions.

The resulting segments provide actionable insights that businesses can use to improve customer engagement, retention, and targeted marketing decisions.

## Author

**Sanket**

**Skills Demonstrated:** Python, Data Cleaning, Exploratory Data Analysis, Feature Engineering, RFM Analysis, Data Transformation, StandardScaler, K-Means Clustering, Customer Segmentation, Business Insights.

