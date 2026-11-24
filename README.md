# Customer Segmentation using RFM & K-Means Clustering

End-to-end data analytics project that segments retail customers into actionable groups based on purchasing behavior using **RFM (Recency, Frequency, Monetary)** analysis and **K-Means clustering**.

## Project Overview

Marketing teams often waste budget treating all customers the same. By grouping customers based on how recently they bought, how often they buy, and how much they spend, businesses can design targeted retention, loyalty, and win-back campaigns.

### Key Steps Covered
1. **Data Cleaning & Preprocessing:** Removed missing `CustomerID` records, filtered out invalid/negative quantities and prices, parsed dates, and calculated `TotalSpend`.
2. **RFM Feature Engineering:** Computed **Recency**, **Frequency**, and **Monetary** metrics for each unique customer.
3. **Transformation & Scaling:** Applied `log1p` transformation to reduce right-skewness and standardized features using `StandardScaler`.
4. **Optimal Cluster Selection ($K$):** Evaluated cluster counts using the **Elbow Method** and **Silhouette Score**.
5. **Segment Profiling & Business Strategy:** Mapped clusters to distinct customer personas with practical marketing recommendations.

## Tech Stack
- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning & Preprocessing:** Scikit-learn (`KMeans`, `StandardScaler`, `silhouette_score`)
- **Visualization:** Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

## Dataset
- **Online Retail Dataset** (UCI Machine Learning Repository / Kaggle) — transactional retail data containing invoice details, product quantities, prices, timestamps, and customer IDs.
- *Note:* Raw dataset files are excluded from this repository due to file size limits. Place `online_retail.csv` inside a local `data/` folder to run the notebook end-to-end.

## Customer Segments & Strategy

| Segment | RFM Profile | Business Action |
| :--- | :--- | :--- |
| **Champions** | Low Recency, High Frequency, High Monetary | VIP loyalty perks, early access to launches, referral rewards |
| **Loyal Customers** | Moderate-Low Recency, High Frequency, Good Spend | Cross-sell/upsell complementary items, membership benefits |
| **At-Risk** | High Recency, Lower Frequency, Notable Past Spend | Personalized win-back offers, re-engagement emails |
| **Dormant / Low Value** | High Recency, Low Frequency, Low Monetary | Low-cost automated reminders or minimal ad spend |

## How to Run Locally

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd customer-segmentation-rfm
