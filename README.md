# Analysis of Sampling Techniques on Imbalanced Credit Card Data

## 1. Project Overview
This project addresses the **Class Imbalance** problem in credit card fraud detection. In such datasets, fraudulent transactions are much fewer than legitimate ones, which can bias the model. We balanced the dataset and evaluated 5 different sampling techniques across 5 machine learning models.

## 2. Methodology
- **Balancing Technique:** Random Oversampling was used to create a 50/50 class distribution.
- **Sampling Methods:** Simple Random, Systematic, Stratified, Cluster, and Bootstrap sampling.
- **Models Evaluated:** Logistic Regression (M1), Random Forest (M2), SVM (M3), Decision Tree (M4), and Extra Trees (M5).

## 3. Performance Visualization
Niche diya gaya graph har sampling technique aur model ki accuracy ko compare karta hai. Yeh graph dikhata hai ki kaunsa model sabse stable raha.

![Model Accuracy Graph](comparison_graph.png)

## 4. Final Accuracy Table (Performance Matrix)
The following table summarizes the accuracy scores (in %) obtained for each model-sampling pair:

| Model / Sampling Technique | Sampling1 | Sampling2 | Sampling3 | Sampling4 | Sampling5 |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **M1: Logistic Regression** | 93.51 | 89.61 | 89.61 | 89.61 | 93.51 |
| **M2: Random Forest** | 100.00 | 100.00 | 98.70 | 98.70 | 100.00 |
| **M3: SVM** | 67.53 | 75.32 | 64.94 | 70.13 | 72.73 |
| **M4: Decision Tree** | 97.40 | 97.40 | 87.01 | 97.40 | 98.70 |
| **M5: Extra Trees** | 100.00 | 100.00 | 100.00 | 100.00 | 100.00 |

## 5. Technical Discussion
* **Top Performers:** **M2 (Random Forest)** and **M5 (Extra Trees)** consistently achieved **100% accuracy**, proving they are the best for this dataset.
* **Observations:** **M3 (SVM)** showed the lowest accuracy and high volatility, meaning it is not suitable for this specific sampled data.
* **Conclusion:** Ensemble tree-based models are highly recommended for fraud detection tasks when data is balanced using oversampling.

---
**Author:** [Your Name]
