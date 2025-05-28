# 🏦 Loan Default Prediction: Probability of Default (PD)

Financial institutions face **significant risks** due to loan defaults. Accurately predicting the **Probability of Default (PD)** is critical for effective **risk management** and **strategic planning**.

🎯 In this project, we develop a machine learning model to estimate the likelihood that a loan will default, based on historical loan data.

---

## 📊 Problem Statement

> Build a predictive model to estimate the **probability of default** for loan applicants using historical loan application data.

---

## 🧭 My Approach

### 📦 1. Package Imports
- Imported all necessary libraries including `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, `shap`, etc.
- Managed long list of packages to support **EDA**, **preprocessing**, **modeling**, and **interpretation**.

---

### 🧮 2. Data Loading & Cleaning
- Fixed **index column issues** in the dataset.
- Dropped **repeated columns** that appeared due to merging or saving errors.

---

### 🔎 3. Exploratory Data Analysis (EDA)

#### ✅ Cleaned Key Columns:
- **`remaining_term`**: Standardized inconsistent values.
- **`job`**: Unified titles and standardized missing entries.
- **`location`**: Cleaned and **grouped underrepresented categories** to avoid data sparsity.
- **`currency`** and **`country`**: Dropped due to low variance and redundancy.
- **`gender`**: Added an explicit `NaN` category to **"Other"** for clarity.

---

### 🏗️ 4. Feature Engineering

- Created new features based on **correlation analysis** with the target (`default`).
- Engineered **interaction features** where relevant.
- Ensured **no data leakage** during feature creation.

---

### 🔧 5. Preprocessing

- 🧠 **Gender Imputation**: Used a **Random Forest classifier** to intelligently impute missing values.
- 🧹 **Simple Imputer**: Applied for other missing categorical/numerical values.
- Scaled numerical features and one-hot encoded categoricals.

---

### 🧪 6. Model Selection

- Evaluated multiple models using **cross-validation**:
  - Logistic Regression
  - Random Forest

---

### 🧬 7. Feature Selection

- Tried **Recursive Feature Elimination (RFE)** but results were **unsatisfactory**.
- Opted for **manual selection** based on domain knowledge and model performance.

---

### 🛠️ 8. Hyperparameter Tuning

- Used **RandomizedSearchCV** for fast and efficient parameter optimization.

---

### 🧠 9. Interpretation

- Applied **SHAP (SHapley Additive exPlanations)** to interpret model predictions.
- Identified key features driving loan default risk:
  - Loan amount
  - Remaining term
  - Employment status
  - Income vs. loan ratio


---

> 🔒 *Note: This project is for educational purposes and should not be used as financial advice or in production without further validation.*
