# Drug-Discovery-Project-collagense_v1

## Objective:
The objective of this project is to predict the **PCI50** value, which represents the **50% probability of collagenase inhibition**. Collagenases are critical enzymes involved in tissue remodeling, wound healing, and pathological ECM degradation. They play a significant role in diseases like cancer, arthritis, and fibrosis. Understanding the inhibition of collagenases and predicting PCI50 values could greatly aid drug discovery, particularly in designing inhibitors for therapeutic applications.

## Key Aspects:
1. **Collagenases as Therapeutic Targets**: Collagenases are essential in various biological processes, including tissue remodeling and wound healing. They also contribute to diseases like cancer and fibrosis. Inhibiting collagenases can be a potential therapeutic approach to treat these diseases.
   
2. **PCI50 (50% Probability of Collagenase Inhibition)**: PCI50 is a quantitative measure indicating the probability at which a compound will inhibit collagenase activity by 50%. Predicting PCI50 is critical for drug discovery, as it helps identify potential collagenase inhibitors.

3. **Dual Role in Drug Discovery**: 
   - **As a drug target**: Collagenases are potential targets for drug development to inhibit excessive tissue degradation in diseases such as arthritis and cancer.
   - **As a therapeutic enzyme**: Collagenases can also be used as therapeutic enzymes to break down damaged tissues in certain medical conditions, such as fibrosis.

4. **Data Source**: The ChEMBL database provides comprehensive data about compounds, their biological activities, and interactions with enzymes like collagenases. This data will be leveraged to build a predictive model for PCI50.

## Problem Statement:
The goal of this project is to use supervised machine learning techniques to predict PCI50 values for various compounds interacting with collagenases. By predicting PCI50, we aim to identify effective inhibitors and therapeutic agents, contributing to drug discovery and medical research.

## Target Outcome:
The desired outcome of this project is to develop a machine learning model that accurately predicts the PCI50 value for compounds interacting with collagenases. This will aid in the discovery of potent inhibitors for collagenase-related diseases, such as cancer and fibrosis.

## Data Features:
The data may include the following features:
- Chemical structure of the compounds
- Biological activity data (e.g., IC50, EC50)
- Molecular descriptors (e.g., molecular weight, polarity)
- Ligand-receptor interaction information

The target variable will be PCI50, which quantifies the likelihood of a compound inhibiting collagenase activity by 50%.

# Model Comparison for pIC50 Prediction

## Results Table
| Model                  | Mean Squared Error (MSE) | R² Score         |
|------------------------|--------------------------|------------------|
| **XGBoost Regression** | 0.3969                  | 0.7475           |
| **Ridge Regression**   | 0.4736                  | 0.6987           |
| **Random Forest**      | 0.4234                  | 0.7305           |
| **Support Vector Regression (SVR)** | 0.587      | 0.6264           |
| **K-Nearest Neighbors (KNN)**        | 0.6477      | 0.5878           |


# Optimized XGBoost Model for Collagenase pIC50 Prediction
![Screenshot from 2025-02-03 11-36-40](https://github.com/user-attachments/assets/4729d5bd-431f-4c96-8cf2-25c9e5df4231)

## Final Results
- **Mean Squared Error (MSE)**: **0.3260**
- **R² Score**: **0.7925**

---

## Discussion of Results

### 1. **Model Performance**
- The optimized XGBoost model achieved a **significant improvement** compared to baseline results, with a lower MSE and higher R².
- The **R² score of 0.7925** indicates that the model explains approximately **79.25% of the variance** in the pIC50 values for collagenase. This reflects high predictive accuracy and reliability.
- The **MSE of 0.3260** suggests that the model's average error in predicting pIC50 is relatively small, which demonstrates that the optimization of hyperparameters (e.g., learning rate, number of estimators, max depth) was effective.

---

### 2. **Biological Implications**
- The accurate prediction of **pIC50 values** is critical for understanding the potency of chemical compounds targeting collagenase enzymes. 
- This result shows the feasibility of utilizing XGBoost as a robust tool for drug discovery tasks, especially when dealing with complex biochemical datasets.

---

### 3. **Feature Importance**
- Key features contributing to the model's predictions include:
  - Structural descriptors (e.g., **MaxEStateIndex, SMR_VSA10, NumHAcceptors**).
  - Physicochemical properties (e.g., **FractionCSP3, SlogP_VSA3**).
- These features play a vital role in defining the interactions of compounds with collagenase, highlighting the significance of molecular descriptors in QSAR modeling.

---

### 4. **Potential Applications**
- This model can help prioritize compounds for further **experimental validation** by identifying potent inhibitors based on their predicted pIC50 values.
- It provides a foundation for integrating machine learning into the **early stages of drug discovery** targeting collagenase or similar enzymes.

---

## Conclusion
The optimized XGBoost model demonstrates strong predictive capability for collagenase pIC50, supporting its application in drug discovery workflows. The results emphasize the importance of feature engineering and hyperparameter tuning to improve model performance in QSAR studies.


