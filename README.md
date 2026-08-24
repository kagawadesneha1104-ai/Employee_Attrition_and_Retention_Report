👥 Employee Attrition & Retention Data Analysis

Employee Attrition & Retention Data Analysis is a Python-based data analytics project focused on analyzing 1,020 employee records across demographic, organizational, salary, performance, employment-status, and remote-work attributes. The project uses Python, Pandas, and Matplotlib to inspect, clean, transform, analyze, and visualize employee data.

The analysis focuses on variables such as age, department/region, employee status, joining date, salary, performance score, and remote work, transforming a messy employee dataset into a structured and analysis-ready dataset.

Note: This project performs employee data analysis and visualization. It does not build a machine-learning attrition prediction model.

![alt text](<visualization/Employee Attrition & Retention Report.png>)


🚀 Core Features

The project implements the following data analytics workflow:

1. Data Loading & Inspection
Loaded the raw employee dataset using Pandas.
Inspected the first and last records.
Checked dataset shape and size.
Examined column names, indexes, and data types.
Used info() and describe() to understand the dataset.
2. Data Selection & Filtering
Selected required columns for analysis.
Used iloc and loc for row-level selection.
Filtered employees based on salary and age.
Filtered employees by department/region.
Applied multiple conditions using AND and OR.
Used isin(), between(), and query() for filtering.
Sorted employees by age, salary, department/region, and name.
3. Data Transformation
Created a bonus column with a fixed bonus value of 5000.
Created Total_salary using salary and bonus.
Updated selected employee salary values.
Updated a selected department/region value.
Prepared the dataset for analysis and visualization.
4. Missing Value Handling
Identified missing values using Pandas.
Calculated missing-value counts.
Calculated the mean of Age.
Demonstrated mean-based filling for missing age values.
Calculated the median of Salary.
Demonstrated median-based filling for missing salary values.
Checked the mode of Department_Region.
Removed rows containing missing values using dropna().
5. Duplicate Record Handling
Checked duplicate records using duplicated().
Counted duplicate records.
Displayed duplicate rows for inspection.
Removed duplicate records using drop_duplicates().
Checked the final dataset shape after duplicate removal.
6. Descriptive Statistics
Calculated total salary.
Calculated average and median salary.
Identified minimum and maximum salary.
Calculated salary standard deviation and variance.
Identified employees with the highest and lowest salary.
Analyzed department/region frequency.
Analyzed remote-work distribution.
Filtered employees above and below the average salary.
7. Data Visualization

Created multiple visualizations using Matplotlib to communicate employee patterns:

Number of Employees by Department
Average Salary by Age
Salary Distribution
Age vs Total Salary
Employee Work Distribution
Employee Performance Score
Employee Status Distribution
8. Clean Dataset Export

The cleaned employee dataset was exported into:

CSV
Excel
JSON
📈 Key Analysis Areas
Analysis Area	Description
Employee Demographics	Examined employee age and basic employee information
Department & Region	Analyzed employee distribution across department/region combinations
Employee Status	Examined Active, Pending, and Inactive employees
Salary Analysis	Calculated salary statistics and identified salary patterns
Total Salary	Added a fixed bonus and calculated total salary
Performance	Analyzed employee performance-score categories
Remote Work	Examined remote and non-remote employee distribution
Age & Salary	Visualized the relationship between age and total salary
Data Quality	Identified and handled missing values and duplicate records
🛠️ Technology Stack
Category	Technology	Description
Language	Python	Core programming and data analysis language
Data Analysis	Pandas	Data loading, cleaning, filtering, transformation, and analysis
Visualization	Matplotlib	Charts and graphical analysis
Dataset	Employee Records	1,020 employee records across 12 columns
Notebook	Jupyter Notebook / Google Colab	Environment used for analysis
Output Formats	CSV, Excel, JSON	Cleaned dataset export formats


📂 Project Structure
Employee_Attrition_and_Retention/
│
├── data/
│   ├── cleaned dataset/
│   │   ├── Cleaned_Employee_dataset.csv
│   │   ├── Cleaned_Employee_dataset.json
│   │   └── Cleaned_Employee_dataset.xlsx
│   │
│   └── raw dataset/
│       └── Messy_Employee_dataset.csv
│
├── notebook/
│   └── Employee_Attrition_and_Retention_Report.ipynb
│
├── presentation/
│   └── Employee_Attrition_and_Retention_Report.pptx
│
├── visualization/
│   ├── Age vs Total Salary.png
│   ├── Average Salary by Age.png
│   ├── Employee Attrition & Retention Report.png
│   ├── Employees Performance Score.png
│   ├── Employees Status Distribution.png
│   ├── Employees Work Distribution.png
│   ├── Number of Employees by Department.png
│   └── Salary Distribution.png
│
└── README.md
🔄 Data Analytics Workflow
Raw Employee Dataset
        ↓
Data Loading
        ↓
Data Inspection
        ↓
Data Selection & Filtering
        ↓
Missing Value Analysis
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
Data Visualization
        ↓
Clean Dataset Export
🔍 Dataset Overview

The dataset contains 1,020 employee records and 12 columns.

The main columns are:

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
Dataset Characteristics
Employee_ID contains employee identifiers.
Age contains employee age values.
Department_Region combines department and region information.
Status contains employee employment-status categories.
Join_Date contains employee joining dates.
Salary contains employee salary information.
Performance_Score contains performance categories.
Remote_Work indicates whether an employee works remotely.
🧹 Data Cleaning & Transformation

The raw employee dataset was prepared for analysis through multiple preprocessing steps.

Missing Values

Missing values were identified using:

df.isnull()
df.isnull().sum()

The analysis calculates:

df["Age"].mean()
df["Salary"].median()
df["Department_Region"].mode()

Mean-based handling was demonstrated for Age, and median-based handling was demonstrated for Salary.

Rows containing missing values were removed using:

df.dropna(inplace=True)
Duplicate Records

Duplicate records were checked using:

df.duplicated()
df.duplicated().sum()
df[df.duplicated()]

Duplicates were removed using:

df.drop_duplicates(inplace=True)
💰 Salary Analysis

Salary analysis was performed using Pandas descriptive-statistics functions.

df["Salary"].sum()
df["Salary"].mean()
df["Salary"].median()
df["Salary"].max()
df["Salary"].min()
df["Salary"].std()
df["Salary"].var()

The project also identifies employees with the highest and lowest salaries:

df[df["Salary"] == df["Salary"].max()]
df[df["Salary"] == df["Salary"].min()]

Salary-based filtering was also performed:

df[df["Salary"] > 70000]
df[df["Salary"] < df["Salary"].mean()]
🎁 Total Salary Calculation

A fixed bonus of 5000 was added to the employee data:

df["bonus"] = 5000

Total salary was then calculated as:

df["Total_salary"] = df["Salary"] + df["bonus"]

The derived Total_salary field was used in salary-related visualizations.

🏢 Department & Region Analysis

Employee distribution was analyzed using:

df["Department_Region"].value_counts()

The project also demonstrates filtering specific department/region combinations:

df[df["Department_Region"] == "Admin-California"]

Multiple conditions were applied, for example:

df[
    (df["Department_Region"] == "Admin-California") &
    (df["Salary"] > 60000)
]

Other filtering techniques include:

df["Department_Region"].isin(
    ["Sales-Nevada", "Admin-California"]
)

df["Salary"].between(40000, 70000)

df.query("Department_Region != 'Sales-Nevada'")
👤 Employee Status Analysis

The dataset contains three employee-status categories:

Active
Pending
Inactive

Status distribution was visualized using Matplotlib.

The analysis helps understand the overall workforce status within the dataset.

🏠 Remote Work Analysis

The Remote_Work column contains Boolean values indicating remote-work status.

The distribution was analyzed using:

df["Remote_Work"].value_counts()

A pie chart was created to visualize the work-mode distribution.

The visualization is stored as Employees Work Distribution.png in the visualization/ folder.

⭐ Employee Performance Analysis

Employee performance was analyzed using the Performance_Score column.

The dataset contains performance categories such as:

Excellent
Good
Average
Poor

The distribution was visualized using a bar chart.

This provides an overview of employee performance categories across the dataset.

📊 Data Visualization

The project includes multiple Matplotlib visualizations.

1. Number of Employees by Department

Shows the number of employee records across the Department_Region categories.

2. Average Salary by Age

Calculates average Total_salary for each employee age:

avg_salary = df.groupby("Age")["Total_salary"].mean()

A line chart is then used to visualize the result.

3. Salary Distribution

A histogram is used to understand the distribution of Total_salary values.

4. Age vs Total Salary

A scatter plot is used to visualize employee age against total salary.

5. Employee Work Distribution

A pie chart is created from the Remote_Work field to show the distribution of remote and non-remote employees.

6. Employee Performance Score

A bar chart displays the number of employees in each performance-score category.

7. Employee Status Distribution

A pie chart displays the distribution of Active, Pending, and Inactive employees.

📤 Cleaned Dataset Export

After cleaning and transformation, the processed dataset was exported into three formats.

CSV
df.to_csv(
    "Cleaned_Employee_dataset.csv",
    index=False
)
Excel
df.to_excel(
    "Cleaned_Employee_dataset.xlsx",
    index=False
)
JSON
df.to_json(
    "Cleaned_Employee_dataset.json",
    orient="records",
    indent=4
)

These files are stored inside:

data/
└── cleaned dataset/
💡 Key Outcomes

The project successfully demonstrates a practical employee data analytics workflow.

Major outcomes:
Analyzed 1,020 employee records.
Worked with 12 employee-related columns.
Performed dataset inspection using Pandas.
Applied row and column selection techniques.
Performed conditional filtering and sorting.
Identified and handled missing values.
Detected and removed duplicate records.
Calculated salary statistics.
Created a bonus field and calculated Total_salary.
Analyzed department/region distribution.
Analyzed employee status.
Analyzed remote-work distribution.
Analyzed employee performance scores.
Created multiple Matplotlib visualizations.
Exported the cleaned dataset into CSV, Excel, and JSON formats.
📦 Requirements
Python
Pandas
Matplotlib
Jupyter Notebook / Google Colab
openpyxl

Install the required libraries:

pip install pandas matplotlib openpyxl jupyter
▶️ Running the Project
1️⃣ Clone the Repository
git clone <your-repository-url>
cd Employee_Attrition_and_Retention
2️⃣ Install Dependencies
pip install -r requirements.txt
3️⃣ Start Jupyter Notebook
jupyter notebook
4️⃣ Open the Analysis Notebook

Open:

notebook/
└── Employee_Attrition_and_Retention_Report.ipynb
5️⃣ Run the Notebook

Run the notebook cells sequentially to reproduce:

Data Loading
↓
Data Inspection
↓
Data Cleaning
↓
Data Transformation
↓
Descriptive Analysis
↓
Visualization
↓
Dataset Export
🎯 Project Objective

The primary objective of this project is to demonstrate a complete Python-based employee data analytics workflow, starting from a messy employee dataset and progressing through data inspection, filtering, cleaning, transformation, descriptive analysis, visualization, and data export.

The project provides a structured foundation for understanding employee workforce patterns related to department/region, salary, status, performance, age, and remote work, and can be extended further for advanced employee attrition and retention analysis.