# DecodeLabs Data Science Project 1
## Advanced EDA & Feature Engineering

### Project Overview

This project focuses on transforming the Student Performance dataset into a clean and analysis-ready dataset through exploratory data analysis, statistical imputation, outlier treatment, and feature engineering.

### Dataset

The project uses the Student Performance dataset from the UCI Machine Learning Repository.

The dataset contains:

- 395 student records
- 33 original columns
- Student demographic, academic, social, and study-related information

### Project Objectives

The main objectives were:

1. Handle missing data using statistical imputation.
2. Detect and neutralize outliers using the Interquartile Range (IQR) method.
3. Engineer at least three new predictive features.
4. Produce a cleaned dataset suitable for further machine learning analysis.

### Missing Data Handling

The original dataset contained no naturally occurring missing values.

To demonstrate the required statistical imputation technique, 20 missing values were intentionally simulated in the `absences` variable.

Median imputation was then applied to replace these simulated missing values.

After imputation:

- Missing values in `absences`: 0

### Outlier Detection and Treatment

The IQR method was applied to the `absences` variable.

Results:

- Q1: 0
- Q3: 8
- IQR: 8
- Lower Bound: -12
- Upper Bound: 20
- Detected outliers: 15

IQR capping was used to neutralize extreme values.

Before treatment:

- Maximum absences: 75

After treatment:

- Maximum absences: 20
- Remaining outliers: 0

### Feature Engineering

Three new features were created:

#### 1. Average_Grade

Calculated as the average of G1, G2, and G3.

#### 2. Grade_Improvement

Calculated as:

G3 - G1

This represents the change in a student's grade between the first and final periods.

#### 3. Study_Absence_Ratio

Calculated using study time and absences:

Study Time / (Absences + 1)

The addition of 1 prevents division by zero.

### Final Dataset

After cleaning and feature engineering:

- Rows: 395
- Columns: 36
- Missing values: 0
- Outliers remaining in `absences`: 0

### Project Files

- `DecodeLabs_Project_1_Advanced_EDA.ipynb` — Complete Jupyter Notebook
- `student_performance.csv` — Original dataset
- `student_performance_cleaned.csv` — Cleaned and feature-engineered dataset
- `README.md` — Project documentation

### Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

### Conclusion

The project transformed the original Student Performance dataset into a cleaner dataset through statistical imputation, IQR-based outlier treatment, and feature engineering. The final dataset contains 395 records and 36 columns and is prepared for further exploratory analysis or machine learning applications.