# Drug Discovery Project: Collagenase Inhibition

[![License](https://img.shields.io/badge/license-Custom-blue.svg)](./LICENSE)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter%20Notebook-orange.svg)](https://jupyter.org/)
[![ChEMBL](https://img.shields.io/badge/Data-ChEMBL-4E6E8E?logo=datadog)](https://www.ebi.ac.uk/chembl/)

A machine learning project for predicting PCI50 (50% probability of collagenase inhibition) using biochemical and molecular data from the ChEMBL database. The goal is to accelerate drug discovery by identifying potential collagenase inhibitors.

---

## 📝 Overview

Collagenases are critical enzymes involved in tissue remodeling, wound healing, and pathological processes like cancer and arthritis. Predicting PCI50 values for candidate compounds helps prioritize molecules for further experimental validation and drug development.

---

## 🎯 Objectives

- Predict the **PCI50** value, representing the probability that a compound inhibits collagenase activity by 50%.
- Compare and optimize machine learning models (XGBoost, Ridge, Random Forest, SVR, KNN) for accurate pIC50 prediction.
- Analyze feature importance and biological implications of model results.

---

## 🔑 Key Highlights

- **Data Source:** ChEMBL database (compound bioactivity and molecular features)
- **Target:** PCI50 (50% probability of collagenase inhibition)
- **ML Models:** XGBoost, Random Forest, Ridge Regression, SVR, KNN
- **Best Model:** Optimized XGBoost (MSE: 0.3260, R²: 0.7925)
- **Key Features:** Structural descriptors, physicochemical properties, ligand-receptor interactions

---

## 📂 Project Structure

```
Drug-Discovery-Project-Collagenases_v1/
│
├── data/                 # Raw and processed datasets
├── notebooks/            # Jupyter notebooks for EDA, modeling, results
├── results/              # Generated plots, model outputs, tables
├── README.md             # Project documentation
├── requirements.txt      # Python dependencies
└── LICENSE
```

---

## 📊 Model Comparison

| Model                            | Mean Squared Error (MSE) | R² Score |
|-----------------------------------|--------------------------|----------|
| **XGBoost Regression**           | 0.3969                   | 0.7475   |
| **Ridge Regression**             | 0.4736                   | 0.6987   |
| **Random Forest**                | 0.4234                   | 0.7305   |
| **Support Vector Regression**     | 0.587                    | 0.6264   |
| **K-Nearest Neighbors (KNN)**     | 0.6477                   | 0.5878   |

### 🏆 Final Optimized XGBoost Model

- **Mean Squared Error (MSE):** 0.3260
- **R² Score:** 0.7925

![XGBoost Results Plot](https://github.com/user-attachments/assets/4729d5bd-431f-4c96-8cf2-25c9e5df4231)

---

## 🚀 Usage

### 1. Clone Repository

```bash
git clone https://github.com/khireddinemahaline/Drug-Discovery-Project-Collagenases_v1.git
cd Drug-Discovery-Project-Collagenases_v1
```

### 2. Setup Environment

Install the required Python packages:

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```
Open and run the notebooks in the `notebooks/` directory.

---

## 🧪 Data & Features

- **Compound Structures**
- **Biological Activity Data (IC50, EC50)**
- **Molecular Descriptors (e.g., molecular weight, polarity)**
- **Ligand-Receptor Interactions**
- **Target Variable:** PCI50

---

## 💡 Results & Discussion

- Optimized XGBoost model explains ~79% of variance in pIC50, showing strong predictive power.
- Key features: MaxEStateIndex, SMR_VSA10, NumHAcceptors, FractionCSP3, SlogP_VSA3.
- Biological implication: Enables rapid identification of promising inhibitors for experimental evaluation.

---

## 📌 References

- [ChEMBL Database](https://www.ebi.ac.uk/chembl/)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- Key literature on collagenase inhibitors (add links as appropriate)

---

## 🚦 Future Work

- Expand dataset with additional bioactivity sources
- Explore deep learning and graph-based models
- Integrate protein structure information for improved predictions

---

## 📄 License

This project is licensed under a [Custom License](./LICENSE).

---

## 🙋‍♂️ Contact

For questions or collaboration, please connect via [LinkedIn](https://www.linkedin.com/in/khireddine-mhalaine/) or open an issue.
