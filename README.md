# Customer Segmentation for Promotional Offers - Clustering

# Project Overview
A leading bank wants to develop a customer segmentation strategy to provide targeted promotional offers to its customers. The bank has collected a dataset that summarizes the activities of users over the past few months. The goal is to identify customer segments based on their credit card usage patterns.

# Table of Contents
* Exploratory Data Analysis (EDA)
* Scaling Justification
* Hierarchical Clustering
* K-Means Clustering
* Cluster Profiles and Promotional Strategies

# 1. Exploratory Data Analysis (EDA)

1.1 Data Description

Rows: 210

Columns: 7

Data Types: All values are of type float64.

Null Values: None

Duplicate Rows: None

Outliers: Outliers were detected in the columns probability_of_full_payment and min_payment_amount. However, the number of outliers is very low and not significant.

Boxplot for outliers:

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/00237a1f-4fbe-4635-abcc-270ecc113f8e)

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/f150e275-a301-4ebf-9971-c622df9c8701)

1.2 Univariate Analysis

Frequency Polygon and Histogram: Used to understand the shape of the distribution.

Violin Plot: Visualized data to understand distribution.

Cumulative Distribution Function (CDF): Plotted to show the distribution of data points.

Example Plots:

Frequency Polygon, Violin Plot, and Cumulative Distribution to understand the shape of the distribution. Cumulative distribution function simply tells us that the sharper it rises, the more the number of data points are.

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/c2fec1a2-8cce-4cfe-8e53-6cab078bbdf8)

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/820874a7-c141-4bb4-9555-d0be79f71af8)

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/4895a6f1-c9ba-4dc8-8829-a06e3709e733)

1.3 Multivariate Analysis

Pair Plot: Displayed relationships between columns.

Scatter Plots: Visualized relationships between pairs of columns.

Correlation Heatmap: Highlighted the correlation between different columns, showing positive and negative correlations.

Example Plots:

Scatter plot for the dataset

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/70969ec9-39e8-413c-b1f7-628bac9590d8)

Correlation Heatmap

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/d0f94d0d-c2d9-4f8f-8113-5677b7920daa)

# 2. Scaling Justification

Necessity: Scaling is essential because the values in the columns have significant differences.

Method: Standard scaling ensures that the values are brought closer to each other.

Reason: Hierarchical clustering relies on distance-based computations, making scaling necessary for accurate results.

# 3. Hierarchical Clustering

3.1 Dendrogram Analysis

Dendrogram: Used to identify the optimal number of clusters.

Optimal Clusters: Based on the dendrogram, 3 clusters were chosen.

Dendogram:

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/516a3685-f9fe-4af2-84c3-dcd5ae3c16cd)

3.2 Cluster Description

Segmentation: By analyzing a single column (spending) we can see that customers who spend high are segmented in Cluster 1, low are segmented in Cluster 2 and customers who lie in between high and low spend are segmented in cluster 3.

Code snippet for cutting hierarchical clusters to form 3 flat clusters:

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/8a6386d4-4632-412e-8e0b-2387dd779c58)

# 4. K-Means Clustering

4.1 Elbow Curve

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/010eb7ab-3919-465d-9333-591d68499b37)

Within Sum of Squares: The elbow curve suggested that the optimal number of clusters is 3.

4.2 Silhouette Score

Code snippet for identifying silhouette score:

![image](https://github.com/nit-stack/Customer-Segmentation-for-Promotional-Offers---Clustering/assets/174468592/bcc2f443-6029-4b40-9060-f79185095d54)

Score: 0.5168, indicating well-distinguished clusters.

# 5. Cluster Profiles and Promotional Strategies

5.1 Cluster Profiles

Cluster 1:

Highest: Average spending, advance payments, probability of full payment, account balance, credit limit, maximum amount spent in one purchase.

Promotions: Gift coupons, priority passes, interest-free EMIs, redeemable bonus points, and free first transaction of the month (subject to limits).

Cluster 3:

Moderate: Falls between Clusters 1 and 2 in most metrics.

Promotions: Encourage transition to Cluster 1 by highlighting lucrative bonuses.

Cluster 2:


Lowest: Average spending, advance payments, probability of full payment, account balance, credit limit, maximum amount spent in one purchase.

Strategies: Implement risk-reducing measures like converting excess dues into loans instead of high interest rates. Promotional strategies should ensure bank security first, then provide incentives for full payment.

# Conclusion

This project successfully identified customer segments based on credit card usage and provided tailored promotional strategies for each segment. By leveraging clustering techniques, the bank can now target its promotional offers more effectively, maximizing customer engagement and satisfaction.
