## Titanic Dataset – Data Cleaning & Preprocessing

###  Objective

The goal of this task is to clean and preprocess the Titanic dataset to prepare it for machine learning. This includes handling missing values, encoding categorical variables, feature scaling, and removing outliers.

---

### Tools & Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn

---

### Dataset Info

- **Source**: [Titanic Dataset on Kaggle](https://www.kaggle.com/datasets/yasserh/titanic-dataset)
- **File used**: `Titanic-Dataset.csv`

---

### Preprocessing Steps

#### 1. **Exploratory Data Analysis**
- Checked column data types, null values, and basic statistics using:
  df.info(), df.describe(), df.isnull().sum()

#### 2. **Handling Missing Values**
- `Age`: Imputed with **median**
- `Embarked`: Filled with **most frequent value**
- `Cabin`: Dropped due to excessive missing values

#### 3. **Encoding Categorical Variables**
- `Sex` and `Embarked` were converted to numerical values using **Label Encoding**

#### 4. **Feature Scaling**
- Applied **StandardScaler** to numerical features:
  - `Age`, `Fare`, `SibSp`, `Parch`
- This transformed the values to have **mean = 0** and **standard deviation = 1**

#### 5. **Outlier Detection & Removal**
- Used **Boxplots** to visualize outliers
- Applied **IQR method** to remove rows with extreme outliers:
  
---

### Final Output

The cleaned and preprocessed dataset has:
- All numerical features scaled
- No missing values
- No extreme outliers
- Categorical columns converted to numbers
