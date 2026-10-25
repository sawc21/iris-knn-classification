# Iris Classification with K-Nearest Neighbors

A hands-on implementation of KNN that classifies Iris flowers using Euclidean distance and majority voting, then compares the predictions with scikit-learn.

## What this project explores

- Implementing distance calculation, neighbor selection, and class voting with NumPy and `Counter`.
- Comparing `k = 1, 3, 5, 7` on the same train/test split.
- Reading confusion matrices and exploring the bias-variance tradeoff.

The notebook uses all four features and all three classes in scikit-learn's bundled Iris dataset: 150 samples, with 120 for training and 30 for testing (`random_state=42`).

## Results

| Neighbors | Custom KNN accuracy | scikit-learn accuracy |
| --- | --- | --- |
| 1 | 100% | 100% |
| 3 | 100% | 100% |
| 5 | 100% | 100% |
| 7 | 96.67% | 96.67% |

These results describe one small, fixed test split. The notebook compares several values of `k` on that test set; it does not perform cross-validation or evaluate a final model on a separate untouched holdout. Features are used without scaling.

## Run it

Use Python 3.14.7, the version used for validation. From the repository root, create a virtual environment and install the direct dependencies.

Windows (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

macOS/Linux:

```sh
python3 -m venv .venv
./.venv/bin/python -m pip install -r requirements.txt
```

Open [knn_iris.ipynb](knn_iris.ipynb) in a Jupyter-compatible editor using that environment. Start from the repository root, restart the kernel, and run all cells in order. The notebook displays confusion matrices and an accuracy comparison plot. [knn_results.csv](knn_results.csv) contains the saved custom-model reference results.

In VS Code, open the notebook, choose **Select Kernel > Python Environments**, and select this repository's `.venv` interpreter. Other Jupyter-compatible editors should use the same interpreter.
