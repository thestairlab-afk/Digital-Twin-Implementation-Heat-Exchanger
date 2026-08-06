# Physics-Informed Machine Learning Pipeline for Plate Heat Exchanger Fouling Detection and Fouling Resistance Prediction

## Overview

This repository contains the complete machine learning pipeline developed for the research paper on **physics-informed fouling diagnosis in plate heat exchangers**. The pipeline performs both:

* **Multi-class fouling severity classification**
* **Continuous fouling resistance prediction**

using operational measurements generated from a physics-based heat exchanger simulator.

The implementation includes automated data preprocessing, feature engineering, leakage prevention, model training, hyperparameter optimization, comprehensive evaluation, explainability analysis, and uncertainty estimation.

---

## Repository Contents

```
.
├── Fouling_Detection_Robust_Pipeline.ipynb
├── data/
│   └── heat_exchanger_dataset.csv
├── figures/
└── README.md
```

---

## Features

* Physics-informed feature engineering
* Automatic data preprocessing
* Missing value handling
* Feature scaling
* Multi-class fouling severity classification
* Fouling resistance regression
* Hyperparameter optimization
* Cross-validation
* Leakage prevention checks
* SHAP explainability
* Permutation feature importance
* Uncertainty estimation
* Publication-quality visualizations

---

## Machine Learning Pipeline

### Data Preprocessing

The notebook automatically performs

* duplicate removal
* missing value verification
* feature scaling
* train/test split
* class balancing (where applicable)
* data leakage detection

---

### Classification Task

The classification model predicts four fouling conditions:

| Class    | Description          |
| -------- | -------------------- |
| Normal   | Clean heat exchanger |
| Low      | Early-stage fouling  |
| Moderate | Medium fouling       |
| High     | Severe fouling       |

Performance is evaluated using

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion Matrix
* Five-fold Cross Validation

---

### Regression Task

The regression model predicts the continuous **fouling resistance**.

Evaluation metrics include

* MAE
* RMSE
* R² Score
* Cross-validation R²
* Prediction error analysis

---

### Explainability

Model interpretability is provided using

* SHAP feature importance
* Permutation feature importance
* Feature contribution analysis

These analyses help identify the operational variables that most strongly influence fouling prediction.

---

## Requirements

The notebook was developed using Python 3.11.

Main packages include

```text
numpy
pandas
scikit-learn
xgboost
matplotlib
shap
scipy
joblib
```

Install all dependencies using

```bash
pip install numpy pandas scikit-learn xgboost matplotlib shap scipy joblib
```

---

## Running the Notebook

1. Clone the repository.

```bash
git clone <repository-url>
```

2. Open

```
Fouling_Detection_Robust_Pipeline.ipynb
```

3. Update the dataset path if required.

4. Execute the notebook from the first cell to the last.

The notebook automatically performs

* preprocessing
* feature engineering
* model training
* hyperparameter optimization
* evaluation
* visualization
* explainability analysis

---

## Expected Outputs

Running the notebook generates

* Classification metrics
* Regression metrics
* Confusion matrix
* ROC curves
* Learning curves
* Feature importance plots
* SHAP summary plots
* Regression prediction plots
* Cross-validation statistics

---

## Reproducibility

To ensure reproducibility

* fixed random seeds are used throughout the pipeline
* train/test data are separated before evaluation
* cross-validation is performed independently of the test set
* leakage checks are incorporated into the preprocessing workflow
* all reported results are generated directly from the notebook

---

## License

This repository is released for academic and research purposes. Please cite the accompanying publication when using this work.

---
STAIR Lab
Department of Electrical Engineering

FAST – National University of Computer and Emerging Sciences (FAST-NUCES)

Islamabad, Pakistan
