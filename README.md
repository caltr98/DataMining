# 🔍 Data Mining Project — Gun Violence & Socio-Political Indicators in the U.S.

This repository contains the full code, analysis, and notebooks behind a comprehensive data mining project on U.S. gun violence, enriched with socio-economic and political context.

📅 **Report Date**: January 8, 2024  
✍️ **Authors**: [Calogero Turco](https://github.com/caltr98), Giovanni Cupitò, Davide Pirolo

---

## 📚 Project Summary

This project analyzes gun violence incidents in the United States using multiple data sources, including:

- **Incidents dataset** (location, casualties, participants, demographics)
- **Election results** per congressional district
- **Poverty data** per state and year

We integrated and cleaned the data, created engineered features, and applied several **clustering**, **classification**, and **time series** techniques to uncover patterns in violent incidents.

---

## 🧪 Tasks and Methodologies

### 1. 📊 Data Understanding & Preparation
- Outlier correction, year fixes, geospatial imputation
- Feature engineering: ratios, demographic indicators, poverty trends
- District-level political dominance and election data integration

### 2. 🔗 Clustering
- **K-Means** (USA + California)
- **DBSCAN**
- **Agglomerative Hierarchical**
- **MBSAS**
- Validated using Silhouette Score, SSE, PCA/t-SNE, and heatmaps

### 3. 🧠 Classification
- **Decision Trees** (rule extraction)
- **Neural Networks**
- **AdaBoost**
- **Rule-Based Classifier**

→ Predicts whether an incident resulted in death, with high precision and recall.

### 4. 📈 Time Series Analysis
- Weekly city-level series of drug-involved gun incidents (352 cities × 208 weeks)
- **Whole Series Clustering** using DTW (TimeSeriesKMeans)
- **Feature-based Clustering**
- **Motif and Anomaly Detection** with Matrix Profiles
- **Shapelet Classification** (with SMOTE and undersampling experiments)

---

## 📈 Results Overview

| Algorithm        | Dataset     | Clusters | Silhouette |
|------------------|-------------|----------|------------|
| K-Means          | California  | 12       | 0.292      |
| K-Means          | USA         | 11       | 0.240      |
| DBSCAN           | California  | 25       | 0.261      |
| Hierarchical     | California  | 9        | 0.266      |
| MBSAS            | USA         | 17       | 0.311      |

✅ **Classification Accuracy**:  
- Decision Tree: ~93% (constrained depth)  
- Neural Network: ~99%  
- AdaBoost: ~99%  
- Rule-Based: ~98%  
- Shapelets: ~50% (due to label imbalance)

---

## ⚠️ GitHub Preview Limitations

> Some notebooks are **too large to preview directly on GitHub** due to rich visual outputs.

### ✅ To view & run(on your dataset, as ours is confidential):
**Google Colab**  
1. Go to [colab.research.google.com](https://colab.research.google.com/)
2. Open the GitHub tab
3. Paste this URL:https://github.com/caltr98/DataMining
4. Select and run the desired notebook.

**Jupyter Notebook (Local)**  
git clone https://github.com/caltr98/DataMining.git
cd DataMining
jupyter notebook

## 📁 Project Files
- `DM_Report.pdf` — Full written report with all methods and analysis

- Jupyter notebooks (please open locally or in Colab):
  - `TASK1/1_Data_Preparation.ipynb`
  - `TASK2/2_Clustering_Analysis.ipynb`
  - `TASK3/3_Classification.ipynb`
  - `TASK4/4_Time_Series_Analysis.ipynb`

---

## 👨‍💻 Authors

- Calogero Turco  
- Giovanni Cupitò  
- Davide Pirolo

---

## 📄 License

This project is licensed under the MIT License — see the LICENSE file for details.
