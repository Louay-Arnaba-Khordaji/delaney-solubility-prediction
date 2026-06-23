# Aqueous Solubility Prediction (logS)

A Python and Scikit-Learn project that implements a **Linear Regression** model to predict the aqueous solubility (`logS`) of chemical compounds based on structural molecular descriptors. 

The program evaluates model performance across split datasets and compares training vs. testing errors to assess predictive accuracy and generalization capabilities.

---

## 📊 Project Features & Workflow

1. **Data Preprocessing:** Loads and parses chemical attributes from the classic Delaney Solubility dataset using `pandas`.
2. **Feature Engineering:** Extracts structural and physical molecular descriptors as inputs ($X$) to predict the target solubility variable ($y$):
   * `MolLogP` (Octanol-Water Partition Coefficient)
   * `MolWt` (Molecular Weight)
   * `NumRotatableBonds` (Molecular Flexibility)
   * `AromaticProportion` (Aromatic Atom Ratio)
3. **Model Implementation:** Builds a Multiple Linear Regression framework utilizing the standard mathematical optimization rule:
   $$\hat{y} = \beta_0 + \beta_1(X_1) + \beta_2(X_2) + \dots + \beta_n(X_n)$$
4. **Validation Setup:** Partitions the underlying matrix into an **80% Training** and **20% Testing** split to ensure proper model validation.
5. **Performance Evaluation:** Computes statistical regression evaluation metrics, including Mean Squared Error (MSE) and Coefficient of Determination ($R^2$ Score), across both dataset splits.

---

## 📁 Repository Contents

```text
delaney-solubility-prediction/
│
├── ML_Project.ipynb                          # Main machine learning workflow (Jupyter Notebook)
├── requirements.txt                          # List of required Python dependency packages
│
├── data/                                     # Output/Input directory for simulation data
│   └── delaney_solubility_with_descriptors.csv # Underlying Delaney solubility chemical dataset
└── README.md                                 # Project documentation
