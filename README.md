# 💳 Credit Card RFM Segmentation + Clustering

This project analyzes credit card transaction data to segment customers using **RFM (Recency, Frequency, Monetary)** metrics. We apply **unsupervised clustering (KMeans)** to group users based on behavior and recommend **targeted marketing strategies** for each segment.

---

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Marketing Strategy](#marketing-strategy)
- [Technologies Used](#technologies-used)
- [How to Run](#how-to-run)

---

## 📌 Project Overview

Understanding customer behavior is key to delivering personalized experiences.  
In this project, we:
- Built an RFM model from raw credit card transactions
- Clustered customers using **KMeans**
- Visualized segments using **PCA**
- Developed strategic insights to help businesses target high-value, at-risk, and new users more effectively

---

## 🧩 Business Problem

Banks and financial services providers often struggle with:
- Retaining high-value customers
- Engaging low-frequency users
- Re-activating dormant or at-risk accounts

By segmenting users based on actual credit card activity, we can drive better decisions around promotions, rewards, and customer engagement.

---

## 📊 Dataset

- **Source:** Synthetic credit card transaction dataset  
- **Size:** ~1M records  
- **Fields Used:**
  - `cc_num` – Customer ID
  - `trans_date_trans_time` – Date of transaction
  - `trans_num` – Transaction ID
  - `amt` – Transaction amount

---

## ⚙️ Methodology

### 1. Preprocessing
- Converted transaction timestamps
- Grouped by customer ID
- Calculated RFM metrics:
  - **Recency**: Days since last transaction
  - **Frequency**: Total number of transactions
  - **Monetary**: Total amount spent

### 2. Feature Engineering
- Removed outliers
- Normalized RFM metrics
- Ran Elbow Method to select `K = 4`

### 3. Clustering
- Applied **KMeans** on scaled data
- Used **PCA** for 2D visualization

### 4. Segment Profiling
- Interpreted each cluster based on RFM behavior
- Connected results to actionable marketing insights

---

## 🔍 Key Findings

| Cluster | Description                  |
|---------|------------------------------|
| 0       | **High Value, Frequent**     |
| 1       | **Inactive or At-Risk**      |
| 2       | **Low Value, Low Frequency** |
| 3       | **New or Growing Potential** |

---

## 📣 Marketing Strategy

- 🎁 **Cluster 0**: Loyalty programs, exclusive perks
- 📬 **Cluster 1**: Win-back campaigns, re-engagement offers
- 🛍 **Cluster 2**: Education, cross-sell & onboarding
- 🚀 **Cluster 3**: Welcome series, nurture content

---

## 🛠 Technologies Used

- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn (KMeans, PCA)
- Jupyter Notebook

---

## ▶️ How to Run

1. Clone this repo  
2. Install dependencies  
3. Run `CreditCard_RFM_Clustering.ipynb`  
4. Replace the dataset path with your own if needed

---

