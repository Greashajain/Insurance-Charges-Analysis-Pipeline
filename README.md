# 🏥  Insurance-Charges-Analysis-Pipeline
A complete preprocessing pipeline for health insurance cost prediction. Includes EDA, data cleaning, feature engineering, feature extraction, and statistical testing to prepare data for machine learning models.


## 📁 Dataset

- **Source**: `insurance.csv` (Kaggle)
- **Rows**: 1,338
- **Columns**:
  - `age`: Age of primary beneficiary
  - `sex`: Gender of the person (male/female)
  - `bmi`: Body Mass Index
  - `children`: Number of children covered by health insurance
  - `smoker`: Smoking status (yes/no)
  - `region`: Residential region in the US
  - `charges`: Individual medical costs billed by health insurance

---

## 🧪 Project Workflow

### 1. 📊 Exploratory Data Analysis (EDA)
- Histograms and boxplots for numeric features
- Count plots for categorical features
- Heatmap for correlation between numerical variables

### 2. 🧹 Data Cleaning
- Removed duplicates
- Checked for missing values (none found)

### 3. 🛠️ Feature Engineering
- Encoded:
  - `sex` → `is_female`
  - `smoker` → `is_smoker`
  - `region` → one-hot encoding
- Created `bmi_category` from BMI values:
  - Underweight, Normal, Overweight, Obese
- Standardized numeric features (`age`, `bmi`, `children`) using `StandardScaler`

### 4. 📈 Statistical Testing
- **Pearson correlation** with `charges` to assess linear relationships
- **Chi-squared tests** for categorical variables to determine statistical significance with `charges`

### 5. 📦 Final Feature Selection
Selected features based on statistical relevance:
- `age`
- `is_female`
- `bmi`
- `children`
- `is_smoker`
- `region_southeast`
- `bmi_category_Obese`
- Target variable: `charges`

---

## 🔧 Tech Stack

- **Python**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **SciKit-Learn**, **SciPy**

