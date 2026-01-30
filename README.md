# Comparative Analysis of Machine Learning Models Using Diverse Sampling Techniques on Imbalanced Financial Data

## 1. Abstract & Introduction
This project investigates the critical challenge of **Class Imbalance** in predictive modeling, specifically within financial fraud detection systems. In such datasets, the 'Fraud' class typically represents a tiny fraction of the total observations, leading standard classifiers to develop a bias towards the majority class. This assignment systematically evaluates how five distinct sampling strategies interact with five different machine learning architectures to identify the most robust combination for fraud detection.

## 2. Dataset Characteristics & Preprocessing
* **Data Source:** The analysis utilizes a credit card transaction dataset where the target variable is highly skewed.
* **Target Variable:** `Class` (0 for Legitimate, 1 for Fraudulent).
* **Balanced Population Generation:** To eliminate initial bias, the dataset was transformed into a **Balanced Population** using the `RandomOverSampler` technique. This ensures a 50:50 distribution, allowing models to learn the nuances of both classes equally before the sampling phase.



## 3. Sampling Methodologies (S1 - S5)
We implemented five statistically significant sampling methods to extract subsets for model training and testing:

1.  **Simple Random Sampling:** Every instance in the balanced population has an equal probability of being selected, ensuring the sample is representative of the whole.
2.  **Systematic Sampling:** Observations are selected at a fixed, predetermined interval ($k$), providing a uniform spread across the data index.
3.  **Stratified Sampling:** The population is divided into strata based on the target class, and samples are drawn to maintain the exact class proportion in the subset.
4.  **Cluster Sampling:** The data is partitioned into distinct groups (clusters), and entire clusters are randomly selected to form the sample.
5.  **Bootstrap Sampling:** A resampling technique with replacement, which is particularly useful for assessing the stability and variance of the machine learning models.

## 4. Machine Learning Framework (M1 - M5)
The following five classifiers were deployed to evaluate the integrity and predictive power of the generated samples:

* **M1: Logistic Regression:** A baseline linear model used to estimate the probability of a binary outcome.
* **M2: Random Forest:** An ensemble bagging method that builds multiple decision trees and merges them to get a more accurate and stable prediction.
* **M3: Support Vector Machine (SVM):** A kernel-based algorithm that searches for the optimal hyperplane to separate the two classes in high-dimensional space.
* **M4: Decision Tree:** A non-linear model that uses a flowchart-like structure to make decisions based on feature values.
* **M5: Extra Trees Classifier:** An extremely randomized tree ensemble that further reduces variance and prevents overfitting better than standard random forests.

## 5. Performance Visualization
The following grouped bar chart illustrates the accuracy trends across all 25 experimental iterations:

![Model Accuracy Graph](graph.png)

## 6. Empirical Results & Performance Matrix
The accuracy scores (in %) for each model-sampling pair are detailed below:

| Model / Sampling Technique | Sampling1 | Sampling2 | Sampling3 | Sampling4 | Sampling5 |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **M1: Logistic Regression** | 93.51 | 89.61 | 89.61 | 89.61 | 93.51 |
| **M2: Random Forest** | 100.00 | 100.00 | 98.70 | 98.70 | 100.00 |
| **M3: SVM** | 67.53 | 75.32 | 64.94 | 70.13 | 72.73 |
| **M4: Decision Tree** | 97.40 | 97.40 | 87.01 | 97.40 | 98.70 |
| **M5: Extra Trees** | 100.00 | 100.00 | 100.00 | 100.00 | 100.00 |

## 7. Technical Discussion & Inference
* **Superior Models:** **M2 (Random Forest)** and **M5 (Extra Trees)** are the most robust performers, consistently achieving near-perfect or 100% accuracy. This suggests that ensemble-based tree methods are best suited for balanced financial datasets.
* **Sampling Stability:** **Sampling1** and **Sampling5** (Random and Bootstrap) provided the most reliable results for the Logistic Regression model, whereas **Sampling3** (Stratified) caused a slight dip in Decision Tree performance.
* **Model Sensitivity:** **M3 (SVM)** proved to be the most volatile model, with its accuracy fluctuating significantly based on the sampling method, indicating a high dependency on specific data distributions.

## 8. Conclusion
The experiment validates that while data balancing is a prerequisite for fraud detection, the **choice of sampling technique** combined with the right **machine learning architecture** is what determines final success. For this specific dataset, tree-based ensemble methods are recommended for maximum reliability.

---
**Author:** [Your Name]  
**Tools:** Python, Scikit-learn, Pandas, Matplotlib  
**Environment:** Google Colab
