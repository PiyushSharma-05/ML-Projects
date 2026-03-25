<h1 align="center">🛒 SmartCart: E-commerce Customer Segmentation</h1>
<p align="center"><i>An Unsupervised Learning approach to data-driven marketing and user profiling.</i></p>

<br>
This project focuses on identifying distinct customer segments within an e-commerce dataset to drive targeted marketing strategies. By applying clustering algorithms, we categorize users based on their purchasing behavior and engagement levels.


<br>
<br>

🚀 Overview
<br>

Dataset: Customer transaction and engagement data.

Goal: Multi-group clustering for personalized marketing (VIP, Retention, Growth).

Key Challenge: Determining the optimal number of clusters (k) and handling feature redundancy.

<br>

🛠️ Technical Workflow
<br>

1. Data Preprocessing & EDA

Imputation: Handled missing values using SimpleImputer to maintain data integrity.

Visualization: Leveraged Pairplots, Heatmaps, and Countplots to identify natural groupings and feature correlations.

Scaling: Applied StandardScaler to normalize features, ensuring distance-based algorithms like K-Means are not biased by units.

<br>

2. Feature Engineering & Optimization
<br>

Dimensionality Reduction: Utilized Principal Component Analysis (PCA) to reduce noise and visualize high-dimensional clusters in 2D/3D space.

Optimal K-Selection: Implemented the Elbow Method using KneeLocator and validated results with Silhouette Scores.

<br>

3. 📊 Segment Analysis & Strategy
<br>

I compared **K-Means**, **DBSCAN**, and **Agglomerative Clustering** to identify the most stable segments. 

> **Technical Note:** During testing, **DBSCAN** generated 30+ clusters and a high volume of noise points, making the segments difficult to decode for business logic. Consequently, I prioritized **K-Means** and **Agglomerative Clustering**, where the number of clusters was pre-decided based on the Elbow Method and Silhouette Analysis.

| Cluster | Behavior Profile | Marketing Strategy (Action Plan) |
| :--- | :--- | :--- |
| **Cluster 0** | High Spend / High Loyalty | **VIP:** Prime services, exclusive loyalty programs. |
| **Cluster 3** | Moderate-High Engagement | **Growth:** Upsell premium features and subscriptions. |
| **Cluster 1** | Low-Moderate / Casual | **Incentivize:** Flash sales and heavy discount coupons. |
| **Cluster 2** | Low Spend / High Risk | **Retention:** Conduct aggressive sales to re-engage. |
| **Cluster 4** | Low Engagement | **Standard:** Normal discount coupons and newsletters. |

<br>
![Customer Segments](02_SmartCart_Unsupervised/final_clusters.png)
<br>

📈 Key Insight
<br>

While K-Means provided the most interpretable segments for business logic, PCA was essential in identifying that spending score and frequency were the primary drivers of variance. Clusters 0 and 3 represent the "Prime" audience, while Clusters 1 and 2 require targeted heavy discounting to prevent churn.

<br>

📂 Project Structure
<br>

SmartCart.ipynb: Fully documented clustering pipeline and analysis.

customer_data.csv: Raw e-commerce behavioral dataset.

cluster_visualization.png: PCA-based cluster distribution plot.