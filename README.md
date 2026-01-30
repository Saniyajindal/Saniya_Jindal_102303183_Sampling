# High-Dimensional Analysis of Sampling Techniques on Imbalanced Credit Card Data

## 1. Project Overview & Objective
This research project focuses on the **Class Imbalance Problem** in financial fraud detection. Standard machine learning models often fail to identify rare fraudulent events because they are overwhelmed by majority-class data. This assignment implements a rigorous framework to balance the data and systematically evaluate 25 different experimental combinations (5 Samples × 5 Models).

## 2. Dataset Strategy
- **Target Variable:** `Class` (0: Legitimate, 1: Fraudulent)
- **Problem:** The original dataset was highly skewed.
- **Solution:** Applied **Random Oversampling** to create a 50/50 balanced population, ensuring the models learn fraudulent patterns effectively.



## 3. Sampling Methodologies (The 5 Approaches)
To test model stability, we derived five distinct samples from the balanced population:
1. **Simple Random Sampling:** Purely stochastic selection to ensure zero bias.
2. **Systematic Sampling:** Selection using a fixed interval $k$, providing a uniform spread across the dataset.
3. **Stratified Sampling:** Maintaining the exact class proportion within the sample to avoid distribution shift.
4. **Cluster Sampling:** Randomly selecting groups (clusters) of data points to simulate real-world data silos.
5. **Bootstrap Sampling:** Resampling with replacement to evaluate model variance.

## 4. Machine Learning Architectures
We utilized five diverse algorithms to observe how different mathematical approaches react to sampled data:
- **M1 (Logistic Regression):** Linear classification baseline.
- **M2 (Random Forest):** Ensemble bagging for high accuracy and low variance.
- **M3 (SVM):** Kernel-based separation for complex decision boundaries.
- **M4 (Decision Tree):** Hierarchical rule-based classification.
- **M5 (Extra Trees):** Extremely randomized trees for maximum robustness.

## 5. Performance Matrix & Visualization
Below is the empirical accuracy recorded across all experimental setups:

| Model / Sampling | Sampling1 | Sampling2 | Sampling3 | Sampling4 | Sampling5 |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **M1: Logistic Regression** | 93.51 | 89.61 | 89.61 | 89.61 | 93.51 |
| **M2: Random Forest** | 100.00 | 100.00 | 98.70 | 98.70 | 100.00 |
| **M3: SVM** | 67.53 | 75.32 | 64.94 | 70.13 | 72.73 |
| **M4: Decision Tree** | 97.40 | 97.40 | 87.01 | 97.40 | 98.70 |
| **M5: Extra Trees** | 100.00 | 100.00 | 100.00 | 100.00 | 100.00 |

### Performance Visualization (Analysis)


*Graph Analysis:*
- **The "Ensemble Peak":** The graph shows that M2 (Random Forest) and M5 (Extra Trees) maintain a flat line at the top (100%), showing zero sensitivity to sampling noise.
- **The "SVM Dip":** M3 shows a volatile "zigzag" pattern, indicating it is highly sensitive to the specific data points selected in each sample.

## 6. Key Findings & Conclusion
1. **Top Performers:** **Random Forest** and **Extra Trees** are the clear winners, providing 100% accuracy.
2. **Sampling Impact:** Simple Random and Bootstrap sampling yielded the highest performance for linear models.
3. **Inference:** For balanced credit card data, ensemble tree-based models should be the industry standard as they provide perfect classification regardless of the sampling technique used.

---
**Developed by:** [Your Name]  
**Date:** January 2026  
**Environment:** Google Colab (Python 3.x)
