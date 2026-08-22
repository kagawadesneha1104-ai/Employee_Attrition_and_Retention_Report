# 👥 Employee Attrition & Retention Data Analysis

**Employee Attrition & Retention Data Analysis** is a Python-based data analytics project focused on analyzing **1,020 employee records** across demographic, organizational, salary, performance, and work-mode attributes. The project uses **Python and Pandas** to load, clean, transform, filter, analyze, and export employee data.

The analysis focuses on variables such as **age, department/region, employee status, joining date, salary, performance score, and remote work status**, transforming a messy employee dataset into a structured and analysis-ready dataset.

---
![alt text](<visualization/Employee Attrition & Retention Report.png>)
## 🚀 Core Features

The project implements the following data analytics workflow:

### 1. **Data Loading & Inspection**

* Loaded the raw employee dataset using Pandas.
* Inspected the first and last records.
* Checked dataset dimensions and total number of elements.
* Examined column names, indexes, and data types.
* Used `df.info()` and `df.describe()` for initial dataset understanding.

### 2. **Data Filtering & Selection**

* Selected specific employee columns for analysis.
* Used `iloc` and `loc` for row-level selection.
* Filtered employees based on salary and age.
* Filtered employees by specific department and region.
* Applied multiple conditions using `AND` and `OR`.
* Used `isin()`, `between()`, and `query()` for efficient filtering.

### 3. **Data Transformation**

* Created a `bonus` column with a fixed bonus value.
* Calculated `Total_salary` using salary and bonus.
* Updated individual employee salary values.
* Updated department/region values where required.
* Prepared the dataset for further analysis.

### 4. **Missing Value Handling**

* Identified missing values using Pandas.
* Calculated missing-value counts.
* Calculated the mean of `Age`.
* Used mean-based filling for missing age values.
* Calculated the median of `Salary`.
* Used median-based filling for missing salary values.
* Checked the mode of categorical department/region values.
* Removed rows containing missing values using `dropna()`.

### 5. **Duplicate Record Handling**

* Identified duplicate records using `duplicated()`.
* Counted duplicate records.
* Displayed duplicate rows for inspection.
* Removed duplicate records using `drop_duplicates()`.
* Validated the resulting dataset shape.

### 6. **Descriptive Statistics**

* Calculated total salary.
* Calculated average and median salary.
* Identified minimum and maximum salary.
* Calculated salary standard deviation and variance.
* Identified employees with the highest and lowest salaries.
* Analyzed department/region frequency.
* Examined remote-work distribution.

### 7. **Data Export**

* Exported the cleaned employee dataset into CSV format.
* Exported the cleaned dataset into Excel format.
* Exported the cleaned dataset into JSON format.

---

## 📊 Key Analysis Areas

| Analysis Area            | Description                                                          |
| :----------------------- | :------------------------------------------------------------------- |
| **Employee Information** | Analyzed employee IDs, names, age, department/region and status      |
| **Salary Analysis**      | Examined salary totals, averages, median, minimum and maximum values |
| **Department & Region**  | Analyzed employee distribution across departments and regions        |
| **Employee Status**      | Examined Active, Pending and Inactive employee records               |
| **Performance**          | Examined employee performance score categories                       |
| **Remote Work**          | Analyzed remote and non-remote employee records                      |
| **Missing Values**       | Identified and handled missing employee data                         |
| **Duplicate Records**    | Detected and removed duplicate employee records                      |
| **Data Filtering**       | Applied conditional filtering based on employee attributes           |
| **Data Transformation**  | Created bonus and total salary fields                                |

---

## 🛠️ Technology Stack

| Category           | Technology                 | Description                                                    |
| :----------------- | :------------------------- | :------------------------------------------------------------- |
| **Language**       | **Python**                 | Core programming and data analysis language                    |
| **Data Analysis**  | **Pandas**                 | Data loading, cleaning, filtering, transformation and analysis |
| **Dataset**        | **Employee Records**       | 1,020 employee records across 12 columns                       |
| **Notebook**       | **Jupyter / Google Colab** | Environment used for performing the analysis                   |
| **Output Formats** | **CSV, Excel, JSON**       | Export formats for the cleaned employee dataset                |

## The notebook loads the dataset using Pandas and works with a **1,020 × 12** structure.

## 📂 Project Structure

```text
employee-attrition-retention/
│
├── data/
│   └── Messy_Employee_dataset.csv       <-- Raw employee dataset
│
├── notebooks/
│   └── Employee_Attrition_and_Retention_Report.ipynb
│                                           <-- Complete analysis notebook
│
├── output/
│   ├── Cleaned_Employee_dataset.csv
│   ├── Cleaned_Employee_dataset.xlsx
│   └── Cleaned_Employee_dataset.json
│
├── README.md
└── requirements.txt
```

---

## 🔄 Data Analytics Workflow

```text
Raw Employee Dataset
        ↓
Data Loading
        ↓
Data Inspection
        ↓
Data Filtering & Selection
        ↓
Missing Value Identification
        ↓
Missing Value Handling
        ↓
Duplicate Detection
        ↓
Duplicate Removal
        ↓
Data Transformation
        ↓
Descriptive Statistics
        ↓
Employee & Salary Analysis
        ↓
Cleaned Dataset Export
```

---

## 🔍 Dataset Overview

The employee dataset contains **1,020 records and 12 columns**.

The main columns include:

```text
Employee_ID
First_Name
Last_Name
Age
Department_Region
Status
Join_Date
Salary
Email
Phone
Performance_Score
Remote_Work
```

The notebook's dataset inspection shows fields covering employee identification, demographic information, department/region, employment status, joining date, salary, contact information, performance score, and remote-work status.

---

## 🧹 Data Cleaning & Transformation

The raw employee dataset was prepared for analysis through multiple preprocessing steps.

### Missing Values

The notebook checks for missing values using:

```python
df.isnull()
df.isnull().sum()
```

Missing values were investigated in columns such as `Age` and `Salary`. The notebook also demonstrates:

```python
df["Age"].mean()
df["Age"].fillna(df["Age"].mean())

df["Salary"].median()
df["Salary"].fillna(df["Salary"].median())
```

Finally, rows containing missing values were removed using:

```python
df.dropna(inplace=True)
```

### Duplicate Records

Duplicate records were checked using:

```python
df.duplicated()
df.duplicated().sum()
df[df.duplicated()]
```

Duplicate records were then removed using:

```python
df.drop_duplicates(inplace=True)
```

The notebook subsequently checks the dataset shape to validate the result.

### Data Transformation

A bonus column was created and used to calculate total salary:

```python
df['bonus'] = 5000

df['Total_salary'] = df['Salary'] + df['bonus']
```

The notebook also demonstrates updating individual employee values and department/region information.

---

## 📋 Employee Data Exploration

Exploratory analysis was performed to understand employee records and their characteristics.

Key operations included:

```python
df.head()
df.tail()
df.shape
df.size
df.columns
df.index
df.dtypes
df.info()
df.describe()
```

The notebook also performs row and column selection using:

```python
df.iloc[10:20]
df.iloc[67]
df.loc[2]
```

These operations help inspect individual employee records and understand the overall structure of the dataset.

---

## 💰 Salary Analysis

Salary analysis was performed using descriptive statistical operations.

Key calculations included:

```python
df["Salary"].sum()
df["Salary"].mean()
df["Salary"].median()
df["Salary"].max()
df["Salary"].min()
df["Salary"].std()
df["Salary"].var()
```

The project also identifies employees with the highest and lowest salaries:

```python
df[df["Salary"] == df["Salary"].max()]
df[df["Salary"] == df["Salary"].min()]
```

Additional salary-based filtering includes:

```python
df[df["Salary"] > 70000]
df[df["Salary"] < df["Salary"].mean()]
```

---

## 🏢 Department & Region Analysis

Employee distribution across departments and regions was examined using:

```python
df["Department_Region"].value_counts()
```

Specific department/region records can also be filtered using conditions such as:

```python
df[df["Department_Region"] == "Admin-California"]
```

Multiple department/region conditions were explored using:

```python
df[
    (df["Department_Region"] == "Admin-California") &
    (df["Salary"] > 60000)
]
```

The project also demonstrates filtering with `isin()` and `query()`.

---

## 🏠 Remote Work Analysis

The dataset contains a `Remote_Work` field indicating whether an employee works remotely.

The distribution was examined using:

```python
df["Remote_Work"].value_counts()
```

This allows the employee population to be separated into remote and non-remote work categories.

---

## 📈 Employee Performance & Status

The dataset includes:

**Employee Status**

```text
Active
Pending
Inactive
```

and **Performance Score** categories such as:

```text
Excellent
Good
Average
Poor
```

These attributes provide a foundation for understanding employee status and performance patterns within the organization.

---

## 📊 Data Analysis Operations

The project demonstrates practical Pandas operations including:

* Column selection
* Row selection
* Conditional filtering
* Multiple-condition filtering
* Sorting
* `isin()`
* `between()`
* `query()`
* `value_counts()`
* Missing-value handling
* Duplicate detection
* Duplicate removal
* Descriptive statistics
* Column creation
* Data modification
* Dataset export

Examples:

```python
df.sort_values("Age")
df.sort_values("Salary")
df.sort_values(["Age", "Salary"])

df["Department_Region"].value_counts()

df["Remote_Work"].value_counts()
```

---

## 📦 Dataset Outputs

After cleaning and analysis, the processed employee dataset is exported into three formats:

```python
df.to_csv("Cleaned_Employee_dataset.csv", index=False)

df.to_excel("Cleaned_Employee_dataset.xlsx", index=False)

df.to_json(
    "Cleaned_Employee_dataset.json",
    orient="records",
    indent=4
)
```

This makes the cleaned data available for further analytics, reporting, visualization, or dashboard development.

---

## 💡 Key Outcomes

The project demonstrates a complete beginner-to-intermediate **Pandas-based employee data analysis workflow**.

### Major outcomes:

* Analyzed **1,020 employee records**.
* Worked with **12 employee-related columns**.
* Inspected employee demographic and organizational information.
* Performed data filtering and conditional selection.
* Identified and handled missing values.
* Detected and removed duplicate records.
* Performed salary-based descriptive statistics.
* Analyzed department/region distribution.
* Examined remote-work categories.
* Created a bonus field and calculated total salary.
* Exported the cleaned dataset into **CSV, Excel, and JSON** formats.
* Built a structured foundation for further employee attrition and retention analysis.

---

## 📋 Requirements

```text
Python
Pandas
Jupyter Notebook / Google Colab
openpyxl
```

Install the required libraries:

```bash
pip install pandas openpyxl jupyter
```

---

## ▶️ Running the Project

### 1️⃣ Clone the Repository

```bash
git clone <your-repository-url>
cd employee-attrition-retention
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Start Jupyter Notebook

```bash
jupyter notebook
```

### 4️⃣ Open the Analysis Notebook

Open:

```text
notebooks/Employee_Attrition_and_Retention_Report.ipynb
```

Run the notebook cells sequentially to reproduce the data loading, cleaning, transformation, analysis, and export workflow.

---

## 🎯 Project Objective

The primary objective of this project is to demonstrate a practical **employee data analytics workflow**, starting from a messy employee dataset and progressing through **data inspection, filtering, cleaning, transformation, descriptive analysis, and dataset export**.

The project demonstrates how Python and Pandas can be used to transform raw employee records into structured, analysis-ready data that can support further **employee attrition, retention, performance, salary, and workforce analysis**.
