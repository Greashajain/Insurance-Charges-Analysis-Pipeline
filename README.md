# Insurance-Charges-Analysis-Pipeline

This project performs a complete **end-to-end analysis pipeline** on a medical insurance dataset to predict the **insurance charges** based on personal attributes such as age, BMI, smoking status, etc.

## 📊 Project Objective

To explore and analyze the medical insurance dataset, engineer meaningful features, perform statistical analysis, and build a regression model to **predict medical charges** accurately.

---

## ⚙️ Tech Stack Used

| Category         | Tools & Libraries                                |
|------------------|--------------------------------------------------|
| Programming      | Python                                           |
| Data Handling    | pandas, numpy                                    |
| Data Visualization | seaborn, matplotlib                            |
| Statistical Analysis | scipy (Pearson & Chi-square tests)          |
| Machine Learning | scikit-learn (Linear Regression, train_test_split) |
| Preprocessing    | StandardScaler, OneHotEncoding (via pandas)     |
| Environment      | Google Colab                  |

---


## 📁 Dataset

- **File:** `insurance.csv`
- **Rows:** 1338
- **Columns:** 7
- **Features:**
  - `age`: Age of the person
  - `sex`: Gender (male/female)
  - `bmi`: Body Mass Index
  - `children`: Number of children/dependents
  - `smoker`: Smoking status (yes/no)
  - `region`: Residential region
  - `charges`: Medical insurance charges (target variable)

---

## 🔧 Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Univariate and multivariate visualizations
- Outlier detection using boxplots
- Correlation heatmap

### 2. Data Cleaning
- Handled duplicates
- Verified missing values
- Converted categorical variables (`sex`, `smoker`, `region`) to numerical formats

### 3. Feature Engineering
- Created `bmi_category` (Underweight, Normal, Overweight, Obese)
- One-hot encoded categorical variables
- Standardized numerical features: `age`, `bmi`, `children`

### 4. Statistical Analysis
- **Pearson Correlation** to assess linear relationships with `charges`
- **Chi-Square Test** for categorical feature relevance

### 5. Model Building
- Used **Linear Regression** from `scikit-learn`
- Split data into training and test sets (80/20)
- Evaluated using **R²** and **Adjusted R²**

### 6. Final Features Used
- `age`, `is_female`, `bmi`, `children`, `is_smoker`, `region_southeast`, `bmi_category_Obese`

---

## 📈 Results

- **R² Score**: ~0.80
- **Adjusted R² Score**: ~0.7988

This indicates a **strong predictive model** that explains ~80% of the variance in insurance charges.

---


