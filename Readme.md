# Glioma Grading Using Machine Learning

> **Project**
> <br />
> Course Unit: [Artificial Intelligence](https://sigarra.up.pt/feup/pt/ucurr_geral.ficha_uc_view?pv_ocorrencia_id=520334), 3rd year
> <br />
> Course: BSc in Informatics and Computing Engineering
> <br />
> Faculty: **FEUP** (Faculty of Engineering of the University of Porto)
> <br />
> Project evaluation: **20**/20

---

## Project Goals

The objective of this assignment was to develop a machine learning classifier to detect Lower-Grade Glioma (LGG) or Glioblastoma Multiforme (GBM). By leveraging clinical features (age, gender, race) and molecular mutation data.

## Methodology

### 1. Data Preprocessing & Exploratory Analysis
We performed an initial analysis of the dataset to check for class distribution and attribute correlation. We addressed missing values and prepared the data for supervised learning by splitting it into training and test sets.

### 2. Feature Selection
To improve the accuracy of our estimators, we explored three distinct dimensionality reduction and feature selection techniques:
* **LASSO (L1-based):** To estimate sparse coefficients and select features with non-zero impact.
* **Tree-based selection:** Using `RandomForestClassifier` to calculate feature importances.
* **Recursive Feature Elimination (RFE):** Iteratively removing the least significant features to identify the optimal subset.

### 3. Model Implementation
We implemented a variety of supervised learning algorithms using the **Scikit-Learn** library:
* **Logistic Regression (LR)**
* **Support Vector Machine (SVM)**
* **K-Nearest Neighbors (KNN)**
* **Random Forest (RF)**
* **AdaBoost**
* **Neural Network (NN)**

### 4. Ensemble Modeling
Following the "No Free Lunch" theorem, we implemented a **Voting Classifier** (soft-voting) to combine the strengths of individual models. Our best-performing ensemble, which combined **SVM, KNN, and NN**, achieved an accuracy of **0.88** on the test data.

## Results Summary

| Model | Accuracy | Precision | Recall |
| :--- | :--- | :--- | :--- |
| **LR** | 0.869 | 0.875 | 0.869 |
| **SVM** | 0.857 | 0.868 | 0.857 |
| **KNN** | 0.827 | 0.829 | 0.827 |
| **RF** | 0.869 | 0.873 | 0.869 |
| **AdaBoost** | 0.857 | 0.868 | 0.857 |
| **NN** | 0.839 | 0.841 | 0.839 |
| **Ensemble** | **0.880** | **0.880** | **0.880** |

## Running the code

**Environment Setup:**
Ensure you have the necessary libraries installed:
```bash
pip install pandas scikit-learn matplotlib seaborn
```

**Running individual models:**
Navigate to the `src/models/` directory and execute the desired script:
```bash
python -m src.models.random_forest
python -m src.models.knn
# ... etc
```

**Feature Selection Analysis:**
To view the results of the different feature selection methods:
```bash
python -m src.feature_selection
```

## Tech Stack

Python, Scikit-Learn, Pandas, Matplotlib, Seaborn

## Team

- Adriano Machado – 202105352
- Diogo Fernandes – 202108752
- João Torre Pereira – 202108848
