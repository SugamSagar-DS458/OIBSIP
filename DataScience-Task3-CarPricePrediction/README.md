# 🚗 Car Price Prediction — Machine Learning Project

## 🔍 Overview

This project builds and compares multiple regression models to estimate a used car's selling price. It was completed as part of a Data Science internship task and demonstrates:

- Data cleaning & handling missing/duplicate values
- Feature engineering (`Car_Age`, `Brand` extraction, brand-name standardization)
- Exploratory Data Analysis with visualizations
- One-Hot Encoding of categorical variables
- Correlation analysis via heatmap
- Training & evaluating **Linear Regression**, **Random Forest Regressor**, and **Gradient Boosting Regressor**
- Feature importance analysis

## 🎥 Demo

[Add a short recording of my work](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task3-CarPricePrediction/Screen%20Recording%202026-08-27%20151112.mp4)


## 📊 Dataset

The dataset used is `car data.csv`, containing details of used cars such as:

| Column | Description |
|---|---|
| `Car_Name` | Name/model of the car |
| `Year` | Year of purchase |
| `Selling_Price` | Price the car is being sold for (target variable) |
| `Present_Price` | Current ex-showroom price |
| `Driven_kms` | Total kilometers driven |
| `Fuel_Type` | Petrol / Diesel / CNG |
| `Selling_type` | Dealer / Individual |
| `Transmission` | Manual / Automatic |
| `Owner` | Number of previous owners |

---

## 🔄 Project Workflow

```mermaid
flowchart LR
    A[Load Dataset] --> B[Data Cleaning]
    B --> C[Feature Engineering]
    C --> D[Exploratory Data Analysis]
    D --> E[One-Hot Encoding]
    E --> F[Train/Test Split]
    F --> G[Model Training]
    G --> H[Model Evaluation]
    H --> I[Feature Importance]
```

**Steps in detail:**

1. **Data Cleaning** — Checked for missing values and duplicate rows; removed duplicates.
2. **Feature Engineering**
   - Created `Car_Age` = 2024 − `Year`
   - Extracted `Brand` from `Car_Name`
   - Standardized inconsistent brand names via a mapping dictionary
   - Standardized `Fuel_Type` casing
3. **EDA** — Visualized selling price distribution, price vs. fuel type, and price vs. car age.
4. **Encoding** — Applied one-hot encoding to categorical columns.
5. **Correlation Analysis** — Heatmap of feature correlations.
6. **Modeling** — Trained and compared:
   - Linear Regression
   - Random Forest Regressor
   - Gradient Boosting Regressor
7. **Evaluation** — Compared models using MAE, RMSE, and R² Score.
8. **Feature Importance** — Visualized top 20 most important features from the Gradient Boosting model.

---

## 🛠 Tech Stack

- **Language:** Python 3.9+
- **Environment:** Jupyter Notebook
- **Libraries:**
  - `pandas`, `numpy` — data manipulation
  - `matplotlib`, `seaborn` — visualization
  - `scikit-learn` — modeling & evaluation

---

## ⚙️ Installation

1. **Clone the repository**

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

2. **Create a virtual environment (recommended)**

```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

3. **Install dependencies**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

```bash
pip install -r requirements.txt
```

```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
scikit-learn>=1.2.0
jupyter>=1.0.0
```

## ▶️ Usage

1. Place the dataset (`car data.csv`) inside a `data/` folder in the project root.
2. Open the notebook:

```bash
jupyter notebook Task3.ipynb
```

3. Update the dataset path in the first cell to point to your local file:

```python
df = pd.read_csv("data/car data.csv")
```

4. Run all cells (**Cell → Run All**) to reproduce the full pipeline — from data cleaning through model evaluation.

---

## 📈 Results

The three models were compared using MAE, RMSE, and R² Score. Example results table (values will vary slightly depending on preprocessing/random seed):

| Model | MAE | RMSE | R² Score |
|---|---|---|---|
| Gradient Boosting Regressor | ✅ lowest error | ✅ lowest error | ✅ highest |
| Random Forest Regressor | Low | Low | High |
| Linear Regression | Higher | Higher | Lower |

> Run the notebook to view the exact metrics printed in the **Model Evaluation** cells and the sorted comparison table.

**Key insight:** Tree-based ensemble models (Random Forest, Gradient Boosting) outperform plain Linear Regression on this dataset, and `Present_Price` and `Car_Age` are typically among the most important predictors of `Selling_Price`.

---

## 🖼 Screenshots

### Selling Price Distribution
![Selling Price Distribution](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task3-CarPricePrediction/Screenshot%202026-08-27%20155415.png)

### Price vs Fuel Type
![Price vs Fuel Type](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task3-CarPricePrediction/Screenshot%202026-08-27%20155441.png)

### Price vs Car Age
![Price vs Car Age](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task3-CarPricePrediction/Screenshot%202026-08-27%20155455.png)

### Correlation Heatmap
![Correlation Heatmap](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task3-CarPricePrediction/Screenshot%202026-08-27%20155751.png)

### Feature Importance
![Feature Importance](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task3-CarPricePrediction/Screenshot%202026-08-27%20155917.png)
```

## 📁 Project Structure

```
├── data/
│   └── car data.csv
├── screenshots/
│   ├── price_distribution.png
│   ├── price_vs_fueltype.png
│   ├── price_vs_age.png
│   ├── correlation_heatmap.png
│   ├── model_comparison.png
│   └── feature_importance.png
├── demo/
│   └── project-demo.mp4 (or .gif)
├── Task3.ipynb
├── requirements.txt
└── README.md
```

## 📬 Contact

```

[GitHub-@SugamSagar-DS458](https://github.com/SugamSagar-DS458)
[LinkedIn-sugamsagar-ai](https://www.linkedin.com/in/sugamsagar-ai/)

```
