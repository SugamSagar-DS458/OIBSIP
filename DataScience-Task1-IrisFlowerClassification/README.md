# Iris Species Classification 🌸

Exploratory data analysis and machine learning classification on the classic **Iris dataset**, built in a Jupyter notebook (`Task_1.ipynb`).

## Overview

This project walks through a complete, lightweight ML workflow:

1. **Load & inspect** the Iris dataset (shape, dtypes, nulls, descriptive stats)
2. **Exploratory Data Analysis (EDA)** — pairplots and box plots to visualize feature distributions across species
3. **Feature importance** analysis using a `RandomForestClassifier`
4. **Model training & evaluation** with two classifiers:
   - Logistic Regression
   - K-Nearest Neighbors (KNN)
5. **Evaluation** via accuracy score, classification report, and confusion matrix for each model

## Dataset

The [Iris dataset](https://scikit-learn.org/stable/datasets/toy_dataset.html#iris-plants-dataset) is loaded directly from `sklearn.datasets`. It contains 150 samples across 3 species (*setosa*, *versicolor*, *virginica*) with 4 numeric features:

- Sepal length (cm)
- Sepal width (cm)
- Petal length (cm)
- Petal width (cm)

## Results

Both **Logistic Regression** and **K-Nearest Neighbors** achieved **100% accuracy** on the held-out test set, with perfect classification reports and confusion matrices (no misclassifications).

## Project Structure

```
.
├── Task_1.ipynb     # Main notebook: EDA, feature importance, model training & evaluation
└── README.md
```

## Requirements

- Python 3.8+
- pandas
- scikit-learn
- seaborn
- matplotlib

Install dependencies:

```bash
pip install pandas scikit-learn seaborn matplotlib
```

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```
2. Launch Jupyter:
   ```bash
   jupyter notebook Task_1.ipynb
   ```
3. Run all cells from top to bottom.

## Workflow Details

| Step | Description |
|------|-------------|
| Data Loading | Loads Iris data into a pandas DataFrame with feature + target columns |
| EDA | Checks shape, dtypes, nulls, and summary statistics |
| Visualization | Pairplot (by species) and box plots per feature |
| Feature Importance | Random Forest used to rank feature importance |
| Train/Test Split | 80/20 split with `random_state=42` for reproducibility |
| Modeling | Logistic Regression and KNN (k=5) classifiers |
| Evaluation | Accuracy, classification report, and confusion matrix heatmaps |
