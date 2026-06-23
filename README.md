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
🛠️ Requirements & Dependencies
Python Environment
Python 3.x

jupyter

Core Data Science Stack
numpy

pandas

scikit-learn

matplotlib

Install all required Python packages via pip:

Bash
pip install -r requirements.txt
🚀 Execution Instructions
Running the Notebook Setup
Clone this repository or download the source directory files locally.

Ensure your dataset is properly stored in the matching path layout: data/delaney_solubility_with_descriptors.csv.

Open your terminal/command prompt inside the repository root directory and launch the environment:

Bash
jupyter notebook
Open ML_Project.ipynb from the browser interface and run the code blocks sequentially.

📈 Data Layout & Model Outputs
The underlying dataset (delaney_solubility_with_descriptors.csv) follows a structured matrix layout:

Feature Columns (1-4): Structural chemical descriptors (MolLogP, MolWt, NumRotatableBonds, AromaticProportion).

Target Column (5): logS (The experimental aqueous solubility measured as the logarithm of molar concentration).

Running the completed model pipeline prints model coefficient weights and metrics directly to the cell outputs:

Training Metrics: Baseline performance values showing how tightly the model fit the training subset.

Testing Metrics: Generalization performance metrics indicating predictive validity on unseen molecules.

🖥️ Visualizing Results
The final cells of the workflow generate a scatter plot comparing Experimental logS (Ground Truth) directly against Predicted logS calculated by the model.

A linear trendline is automatically computed and superimposed onto the plot using numpy.polyfit. A perfect model prediction pipeline would see all data points clustered perfectly along this diagonal progression vector.

🧰 Tech Stack
Language: Python

Machine Learning API: Scikit-Learn (sklearn)

Libraries: Pandas, NumPy, Matplotlib, Jupyter

Environment: Jupyter Notebook / Anaconda

👥 Authors
Louay Arnaba Khordaji
