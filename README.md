# Credit Card Customer Segmentation

## 📖 Overview  
This project performs behavioral and credit‐feature–based segmentation of credit card customers using K-Means clustering. By cleaning, exploring, and reducing the dimensionality of the original data, we identify distinct customer groups to support targeted risk management and personalized marketing strategies.

---

## Repository Structure  
```
├── data/  
├── notebooks/              
│   └── kmeans_clustering.ipynb  
├── reports/                
└── README.md             
```

## 🗄️ Dataset  

- **Source**: Kaggle “Customer Segmentation” (8951 rows × 18 features)  
- **Key Features**:  
  - `BALANCE`, `BALANCE_FREQUENCY`, `PURCHASES`, `ONEOFF_PURCHASES`,  
    `INSTALLMENTS_PURCHASES`, `CASH_ADVANCE`, `PURCHASES_FREQUENCY`,  
    ...and more behavioral & credit indicators.

---

## 🧹 Data Preprocessing  

1. **Missing Values**  
   - Dropped rows missing `CREDIT_LIMIT`; filled `MINIMUM_PAYMENTS` with column median.  
2. **Outlier Treatment**  
   - Identified via IQR and z-score; clipped extreme values to upper/lower whiskers.  
3. **Exploratory Analysis**  
   - Univariate distributions, boxplots, scatter matrices & correlation heatmap to understand feature relationships.

---

## 📏 Dimensionality Reduction (PCA)  

- Applied PCA to retain top 5 components, preserving 95.5% of total variance (PC1–PC2 ≈ 65.3%).  

---

## 🔍 Clustering (K-Means)  

1. **Optimal k Selection**  
2. **Model Training**  
3. **Cluster Assignment**  

---

## 📊 Evaluation  

- **Silhouette Score**: 0.5177  
- **Calinski–Harabasz Score**: 2862.23

---

## 📈 Results & Cluster Profiles  

| Cluster | Key Characteristics                                           |
| ------- | ------------------------------------------------------------- |
| **0**   | Medium‐usage customers; balanced spending & cash advances.    |
| **1**   | Low consumption, high full-payment ratio; conservative users. |
| **2**   | High cash-advance frequency/amount; short-term financers.     |
| **3**   | Very high spending & transaction count; premium customers.    |
| **4**   | Low activity across all metrics; long-standing but inactive.  |

