# Exploratory Data Analysis (EDA) -- Loan Approval Dataset

## Project Overview

This project explores and prepares a loan approval dataset using Python.
The Jupyter Notebook (`EDA.ipynb`) focuses on data cleaning, outlier
handling, encoding categorical variables, transforming distributions,
and scaling numerical features.

## Dataset

-   **Dataset file:** `loan_approved.csv`
-   **Purpose:** Loan approval analysis
-   The notebook loads the dataset with `pandas.read_csv()`.

> Keep `loan_approved.csv` in the same folder as `EDA.ipynb` before
> running the notebook. The CSV file is required and is not included
> unless you add it to this repository.

## Tools and Libraries

-   Python
-   Jupyter Notebook
-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   SciPy
-   Scikit-learn

## Work Covered

### 1. Data Loading and Initial Inspection

-   Import the required Python libraries.
-   Load the CSV dataset into a Pandas DataFrame.
-   Inspect the dataset and check missing-value counts.

### 2. Handling Missing Values

The notebook fills missing values in selected columns: - `Gender` -
`Credit_History` - `LoanAmount` - `Married` - `Self_Employed` -
`Loan_Amount_Term` - `Dependents`

It then checks the missing-value counts again.

### 3. Outlier Detection and Treatment

-   Visualize distributions and potential outliers using boxplots.
-   Apply Winsorization to `ApplicantIncome`.
-   Calculate Q1, Q3, and the interquartile range (IQR) for
    `LoanAmount`.
-   Calculate the lower and upper IQR bounds and filter values outside
    those bounds.
-   Use a boxplot to inspect the result.

### 4. Categorical Encoding

The notebook demonstrates: - **One-hot encoding** using
`pandas.get_dummies()`. - **Label encoding** using Scikit-learn's
`LabelEncoder`. - **Ordinal encoding** using Scikit-learn's
`OrdinalEncoder` (the notebook defines an education order).

### 5. Distribution Visualization and Transformation

Use Seaborn histograms with KDE curves to inspect numerical columns,
including: - `CoapplicantIncome` - `ApplicantIncome` - `LoanAmount` -
`Loan_Amount_Term`

The notebook demonstrates: - Log transformation - Exponential/power
transformation - Square-root transformation - Box-Cox transformation

### 6. Feature Scaling

The notebook applies three scaling techniques to `ApplicantIncome`: -
Standard scaling (`StandardScaler`) - Min-max scaling (`MinMaxScaler`) -
Robust scaling (`RobustScaler`)

## Repository Structure

``` text
.
├── EDA.ipynb
├── loan_approved.csv
└── README.md
```

## How to Run

1.  Clone or download this repository.

2.  Make sure `EDA.ipynb` and `loan_approved.csv` are in the same
    directory.

3.  Install the required libraries:

    ``` bash
    pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
    ```

4.  Start Jupyter Notebook:

    ``` bash
    jupyter notebook
    ```

5.  Open `EDA.ipynb` and run the cells from top to bottom.

## Project Goal

The goal of this notebook is to practice common EDA and
data-preprocessing techniques and understand how missing values,
outliers, categorical variables, feature distributions, and feature
scales can be handled before machine-learning work.

## Note

This notebook demonstrates exploratory analysis and preprocessing
techniques. It does not, in its current form, train or evaluate a
loan-approval prediction model.
