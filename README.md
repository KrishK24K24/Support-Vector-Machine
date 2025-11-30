# Support Vector Machine (SVM) Notebooks

This repository contains Jupyter notebooks that demonstrate SVM for classification and regression, and how kernels affect SVM behavior.

Files
- `SVMClassifier.ipynb` — Classification workflow using SVC (support vector classifier).
- `SVMKernel.ipynb` — Experiments comparing kernels (linear, polynomial, RBF) and visualizing decision boundaries.
- `SVMRegression.ipynb` — Regression workflow using SVR (support vector regression).

What the notebooks do — step-by-step
1. Data loading & EDA
   - Load a dataset (often classic datasets like Iris, a synthetic dataset, or a provided CSV).
   - Inspect distributions, class balance, and visualize features.

2. Preprocessing
   - Handle missing values (if any).
   - Encode categorical features (if present).
   - Scale features using StandardScaler (important for SVMs).

3. Train / Test split
   - Split dataset into training and test sets (typically with `train_test_split`).

4. Model training
   - `SVMClassifier.ipynb`: Train an SVC, check baseline accuracy, use cross-validation, and tune `C`, `gamma`, and kernel via GridSearchCV.
   - `SVMKernel.ipynb`: Train SVCs with different kernels and visualize decision boundaries to show kernel effects.
   - `SVMRegression.ipynb`: Train SVR, tune hyperparameters, and evaluate regression metrics.

5. Evaluation & visualization
   - Classification: accuracy, confusion matrix, classification report, cross-validation scores, and plots of decision boundaries.
   - Regression: Mean Squared Error (MSE), R², scatter plot of predicted vs actual.

Quick start (recommended)
1. Create and activate a virtual environment.
2. Install dependencies:
   pip install numpy pandas scikit-learn matplotlib seaborn jupyter

3. Start Jupyter:
   jupyter notebook
   # or
   jupyter lab

4. Open the notebooks and run cells from top to bottom.

Notes & suggestions
- Scaling features is crucial for SVMs (StandardScaler used in notebooks).
- Use GridSearchCV or RandomizedSearchCV to tune `C`, `gamma`, and kernel parameters.
- For large datasets, consider using a linear kernel or a linear SVM implementation (LinearSVC) for performance.
