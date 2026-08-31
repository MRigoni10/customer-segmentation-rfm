# E-Commerce Customer Segmentation (RFM + K-Means)

Unsupervised customer segmentation on real transaction data to group customers by purchasing behavior and tailor marketing actions.

## Overview
Instead of treating all customers the same, this project segments an e-commerce customer base using the **RFM (Recency, Frequency, Monetary)** framework combined with **K-Means clustering**.

## Steps
1. **Data Cleaning:** Removed cancellations, invalid price entries, and transactions without customer IDs.
2. **RFM Metrics:**
   - **Recency:** Days since last purchase.
   - **Frequency:** Number of unique orders.
   - **Monetary:** Total spending.
3. **Data Prep:** Applied log transformation (`np.log1p`) and `StandardScaler` to handle right-skewed distributions.
4. **Clustering:** Selected $k=4$ clusters based on Elbow Method and Silhouette Score evaluation.

## Segments & Marketing Actions
![RFM Clusters](rfm_clusters_chart.png)

- **Champions:** High spend, frequent, recent buyers. -> *VIP perks, early access, no heavy discounting.*
- **Loyal:** Consistent repeat buyers. -> *Cross-sell and bundle promotions.*
- **At Risk:** High past spenders who haven't bought recently. -> *Win-back email sequences with targeted discounts.*
- **Hibernating:** Infrequent, low spend, inactive. -> *Low-cost automated re-engagement only.*

## Quickstart
Clone the repo and run `rfm_segmentation.ipynb` in Colab or Jupyter.

## How to Run the Project
The complete code is available in the interactive notebook. You can run it with a single click:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]((https://colab.research.google.com/drive/1PfD9MlRjbiyO-5Dge-Mj5_Fkp_Po0Ow7))
