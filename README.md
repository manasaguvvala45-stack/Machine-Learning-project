# Heart Disease Risk Prediction (Framingham Dataset)

Predicting 10-year risk of Coronary Heart Disease (CHD) using the Framingham Heart Study dataset. This project covers data cleaning, exploratory data analysis (EDA), and preprocessing as a foundation for building classification models.

## Dataset

The [Framingham Heart Study dataset](https://www.kaggle.com/datasets/aasheesh200/framingham-heart-study-dataset) contains demographic, behavioral, and medical risk factor data for patients, with the goal of predicting `TenYearCHD` (whether the patient develops coronary heart disease within 10 years).

**Features include:**
- Demographic: `male`, `age`, `education`
- Behavioral: `currentSmoker`, `cigsPerDay`
- Medical history: `BPMeds`, `prevalentStroke`, `prevalentHyp`, `diabetes`
- Clinical measurements: `totChol`, `sysBP`, `diaBP`, `BMI`, `heartRate`, `glucose`
- Target: `TenYearCHD` (0 = no CHD in 10 years, 1 = CHD in 10 years)

## Project Workflow

1. **Data Loading & Inspection** — loaded the dataset and explored its shape, structure, and summary statistics.
2. **Missing Value Handling** — checked for nulls and imputed missing numeric values with column means.
3. **Duplicate Removal** — identified and dropped duplicate records.
4. **Exploratory Data Analysis** —
   - Distribution histograms for all features
   - Class balance check on `TenYearCHD`
   - Gender distribution
   - Age vs CHD risk (boxplot)
   - Correlation heatmap across all features
   - Outlier inspection on key clinical variables (age, cholesterol, blood pressure, BMI)
5. **Train-Test Split** — split data into 80% training / 20% testing sets.
6. **Feature Scaling** — standardized features using `StandardScaler`.

## Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

## Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Running the notebook
1. Clone this repository
2. Download the Framingham dataset and place it in the project directory
3. Update the file path in the notebook to point to your local copy of the dataset
4. Run the notebook cells in order:
```bash
jupyter notebook project.ipynb
```

## Next Steps

- Train and evaluate classification models (e.g., Logistic Regression, Random Forest, XGBoost) on the preprocessed data
- Handle class imbalance in `TenYearCHD` (e.g., SMOTE, class weighting)
- Evaluate using precision, recall, F1-score, and ROC-AUC (accuracy alone is misleading on imbalanced medical data)
- Perform feature importance analysis to identify key CHD risk factors

## License

This project is open source and available under the MIT License.
