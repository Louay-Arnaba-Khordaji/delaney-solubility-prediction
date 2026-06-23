# delaney-solubility-prediction
A machine learning project using Linear Regression to predict chemical aqueous solubility based on molecular properties.
# Predicting Aqueous Solubility (logS) Using Linear Regression

This repository contains a machine learning workflow to predict the aqueous solubility (`logS`) of chemical compounds based on their molecular descriptors using the classic **Delaney Solubility Dataset**.

## 📊 Dataset Description
The dataset contains chemical properties for various molecular compounds:
* **MolLogP:** Octanol-water partition coefficient (measures fat solubility).
* **MolWt:** Molecular weight of the compound.
* **NumRotatableBonds:** Number of freely rotating single bonds (flexibility).
* **AromaticProportion:** Proportion of heavy atoms that are part of an aromatic ring.
* **logS (Target):** The experimental aqueous solubility (logarithm of molar concentration).

## 🛠️ Project Workflow
1. **Data Loading & Exploration:** Inspected features and statistical distributions using `pandas`.
2. **Data Splitting:** Partitioned the dataset into an 80/20 train-test split using `scikit-learn`.
3. **Model Implementation:** Built a `Linear Regression` model to capture linear relationships between molecular descriptors and solubility.
4. **Evaluation:** Evaluated performance across both training and test subsets using Mean Squared Error (MSE) and $R^2$ Score.

## 🚀 How to Run the Project

### 1. Clone the repository:
```bash
git clone [https://github.com/Louay-Arnaba-Khordaji/delaney-solubility-prediction.git](https://github.com/Louay-Arnaba-Khordaji/delaney-solubility-prediction.git)
cd delaney-solubility-prediction

