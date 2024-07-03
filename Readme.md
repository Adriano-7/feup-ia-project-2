# Glioma Grading Using Machine Learning

This project aims to develop a machine learning classifier model to detect Lower-Grade Glioma (LGG) or Glioblastoma Multiforme (GBM) based on clinical and molecular/mutation features obtained from DNA tests.

## Problem Statement

Gliomas are the most common primary brain tumors. They can be graded as LGG or GBM depending on histological/imaging criteria, clinical factors, and molecular/mutation factors. Our goal is to determine whether a patient has LGG or GBM using given clinical and molecular/mutation features, potentially reducing the need for expensive molecular tests.

## Dataset

The dataset combines two genome atlas databases:
- The Cancer Genome Atlas (TCGA)
- The Chinese Glioma Genome Atlas (CGGA)

### Features:
- Clinical features: Gender, Age at diagnosis, Race
- Molecular features: IDH1, TP53, ATRX, PTEN, EGFR, CIC, MUC16, PIK3CA, NF1, PIK3R1, FUBP1, RB1, NOTCH1, BCOR, CSMD3, SMARCA4, GRIN2A, IDH2, FAT4, PDGFRA
- Class feature: Grade (LGG or GBM)

## Methodology

1. Data Preprocessing
2. Feature Selection
   - LASSO L1-based feature selection
   - Tree-based feature selection
   - Recursive feature elimination
3. Model Implementation
   - Logistic Regression (LR)
   - Support Vector Machine (SVM)
   - K Nearest Neighbors (KNN)
   - Random Forest (RF)
   - AdaBoost
   - Neural Network (NN)
4. Ensemble Modeling
   - Voting Classifier

## Results

The best-performing individual models were Neural Network and Random Forest. The best ensemble model, combining SVM, KNN, and NN, achieved an accuracy of 0.88 on the test data.

## Conclusion

This study highlights optimal feature subsets and ensemble strategies for glioma grading, potentially improving clinical decision-making and personalized treatments for glioma patients.

## Tools Used

- Python
- Scikit-Learn
- Pandas
- Matplotlib

## Contributors

- Adriano Machado – 202105352
- Diogo Fernandes – 202108752
- João Torre Pereira - 202108848

Check the [notebook](glioma_segmentation.ipynb) for the code and the results.
