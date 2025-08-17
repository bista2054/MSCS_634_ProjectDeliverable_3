# MSCS_634_ProjectDeliverable_3
This lab builds the classification and clustering models, apply association rule mining, and perform hyperparameter tuning to improve model performance.

## 📌 Project Overview  
This project analyzes global economic indicators from World Bank data (2025). The analysis covers three main tasks:  

1. **Classification** – Predicting whether a country has *high* or *low* GDP per capita.  
2. **Clustering** – Grouping countries into economic clusters based on macroeconomic indicators.  
3. **Association Rule Mining** – Discovering strong relationships between fiscal and economic performance factors.  

---

## 🔍 Key Insights  

### **1. Classification (Random Forest & SVM)**  
- Random Forest achieved **~89% accuracy** with strong precision/recall balance.  
- SVM performed slightly lower (**~84% accuracy**) but still showed consistent predictive ability.  
- Important predictive features included:  
  - **GDP Growth (% Annual)**  
  - **Government Expense (% of GDP)**  
  - **Public Debt (% of GDP)**  
  - **Tax Revenue (% of GDP)**  
  - **Unemployment Rate (%)**  
- Hyperparameter tuning improved Random Forest performance and confirmed feature importance.  

**Takeaway:**  
Macroeconomic stability (low unemployment, balanced fiscal spending, and sustainable debt) is strongly predictive of higher GDP per capita.  

---

### **2. Clustering (K-Means with PCA Visualization)**  
- Optimal cluster size: **k = 3**  
- Country clusters:  
  - **Cluster 0:** High unemployment, moderate GDP, weaker economic health.  
  - **Cluster 1:** Lower unemployment, smaller economies, stronger GDP growth.  
  - **Cluster 2:** Wealthier nations with the highest GDP per capita but high public debt.  
- PCA visualization showed clear separation of these clusters.  

**Takeaway:**  
Countries can be grouped into distinct "economic models" – fast-growing but smaller economies, highly indebted wealthy nations, and vulnerable middle-tier economies.  

---

### **3. Association Rule Mining (Apriori Algorithm)**  
- Strong fiscal performance indicators (high **tax revenue** and **government revenue**) consistently co-occur with high **GDP** and **GDP per capita**.  
- High government efficiency measures are strongly linked to sustainable economic wealth.  
- Lift values > 5 indicate very strong co-occurrence of fiscal and economic health indicators.  

**Takeaway:**  
**Fiscal strength (taxation + revenue collection) is a cornerstone of national economic wealth.** Nations with stronger fiscal frameworks almost always align with higher economic output and prosperity.  

---

## 🌍 Practical Relevance & Applications  
- **Policy-making:** Guide governments on which levers (tax revenue, unemployment, fiscal balance) most strongly drive prosperity.  
- **Investment strategy:** Help investors identify clusters of stable vs. vulnerable economies.  
- **Development planning:** Support international organizations (IMF, World Bank) in tailoring recommendations to cluster-specific challenges.  
- **Early warning systems:** Classification models can detect when a country risks slipping into "low GDP" conditions.  

---

## ⚠️ Challenges & Solutions  

- **Deprecation & Library Updates:** Some modules and functions (e.g., `pd.qcut` or older mlxtend features) caused warnings or errors.  
  - ✅ *Fixed by updating function usage and removing deprecated arguments.*  

- **Feature Engineering:** Key indicators like Government Efficiency and Economic Health were not in the raw data.  
  - ✅ *Engineered these features directly from fiscal and macroeconomic metrics.*  

- **Model Interpretability:** Random Forest and SVM can be “black boxes.”  
  - ✅ *Added feature importance, PCA for clustering, and association rules for transparency.*  
---