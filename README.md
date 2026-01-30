# Assignment - Sampling Techniques on Imbalanced Data

## 1. Objective
[cite_start]The objective of this assignment is to understand the importance of sampling techniques in handling imbalanced datasets[cite: 9]. [cite_start]We analyze how different sampling strategies affect the performance of various machine learning models when applied to a balanced version of a credit card fraud dataset[cite: 9, 11].

## 2. Problem Statement
[cite_start]The dataset used is a highly imbalanced credit card dataset[cite: 11]. Since imbalance can significantly degrade model performance, the task involves:
1. [cite_start]Converting the dataset into a balanced class dataset[cite: 17].
2. [cite_start]Creating five different samples using various techniques[cite: 18].
3. [cite_start]Evaluating five different ML models on these samples to find the best accuracy[cite: 12, 19, 20].

## 3. Methodology
- [cite_start]**Data Balancing:** The original dataset was balanced using oversampling to ensure equal class representation[cite: 12, 17].
- [cite_start]**Sampling Techniques (S1-S5):** Five samples were generated: Simple Random, Systematic, Stratified, Cluster, and Bootstrap sampling[cite: 18, 19].
- [cite_start]**ML Models (M1-M5):** Five models were tested: Logistic Regression (M1), Random Forest (M2), SVM (M3), Decision Tree (M4), and Extra Trees (M5)[cite: 20].

## 4. Final Accuracy Table (Performance Matrix)
[cite_start]The following table summarizes the accuracy results (in %) obtained from the execution[cite: 21]:

| Model / Sampling Technique | Sampling1 | Sampling2 | Sampling3 | Sampling4 | Sampling5 |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **M1 (Logistic Regression)** | 93.51 | 89.61 | 89.61 | 89.61 | 93.51 |
| **M2 (Random Forest)** | 100.00 | 100.00 | 98.70 | 98.70 | 100.00 |
| **M3 (SVM)** | 67.53 | 75.32 | 64.94 | 70.13 | 72.73 |
| **M4 (Decision Tree)** | 97.40 | 97.40 | 87.01 | 97.40 | 98.70 |
| **M5 (Extra Trees)** | 100.00 | 100.00 | 100.00 | 100.00 | 100.00 |

## 5. Discussion & Conclusion
[cite_start]After analyzing the results[cite: 22]:
- [cite_start]**Highest Accuracy:** Both **Random Forest (M2)** and **Extra Trees (M5)** achieved 100% accuracy on several samples[cite: 21].
- [cite_start]**Best Sampling:** Sampling1, Sampling2, and Sampling5 proved most effective for the top models[cite: 21].
- **Conclusion:** Ensemble tree-based models (M2 and M5) outperformed others on this balanced dataset. The choice of sampling technique plays a vital role in model consistency.

---
**Submission by:** [Saniya Jindal]  
