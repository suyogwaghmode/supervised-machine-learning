# Supervised Learning

This folder contains a Jupyter Notebook that demonstrates supervised learning techniques applied to a materials informatics problem (predicting whether a material is metallic using the Matbench `is_metal` dataset).

**What’s included**

- `Supervised Learning.ipynb` — full notebook with data loading, feature engineering (MAGPIE-style features via `matminer`), model training (Random Forest, Gradient Boosting, HistGradientBoosting, SVM, SGD), hyperparameter tuning with `GridSearchCV`, and model interpretation using `shap`.

**Highlights**

- Simple data preprocessing and feature engineering using `matminer` and `pymatgen`.
- Comparison of tree-based vs. distance-based models (scaling notes and when to apply StandardScaler).
- Hyperparameter tuning (grid search) and evaluation (accuracy, F1, ROC AUC, confusion matrix).
- Model interpretability using SHAP values and summary plots — shows which elemental features drive predictions.
- Clear, reproducible notebook that walks through analysis steps and visualizations.

**Key dependencies**

- numpy, pandas
- scikit-learn
- matplotlib, seaborn
- jupyterlab / notebook
- matminer
- pymatgen
- shap

**Notes & dataset**

- The notebook uses the Matbench `matbench_expt_is_metal` dataset (loaded via `matminer.datasets.load_dataset`). The notebook creates a `composition_obj` column and applies MAGPIE element featurizers which may take several minutes depending on your machine.
- Tree-based models do not require scaling; kernels and distance-based methods (SVM, KNN) do — the notebook demonstrates both cases.

**Contact / Attribution**

- Author: (Suyog Waghmode)

**Linked files**

- `results/confusion_matrix.png`
- `results/shap_summary.png`
- `requirements.txt` — environment packages list next to the notebook for reproducibility.

---

