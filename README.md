
# Fashion Retail Sales Data ETL Pipeline

## 📌 Project Description

The Fashion Retail Sales Data ETL Pipeline is a Python-based data engineering project designed to extract, clean, transform, and load fashion retail sales data. The project processes raw sales information from a CSV dataset and prepares it for further analysis.

It handles missing values, identifies and manages outliers, encodes categorical variables, extracts date-related features, and standardizes numerical data. Finally, the transformed dataset is saved into a new CSV file.

This project demonstrates the practical implementation of the ETL (Extract, Transform, Load) process using Python and popular data processing libraries.

## 🎯 Project Objectives

- Extract raw fashion retail sales data from CSV files.
- Handle missing values in the dataset.
- Identify and manage outliers.
- Convert categorical data into numerical format.
- Extract day, month, and year from purchase dates.
- Standardize numerical features.
- Save the processed dataset into a new CSV file.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## 📂 Project Structure

```text
Fashion-Retail-Sales-ETL-Pipeline/
│
├── Fashion_Retail_Sales.csv
├── extract.py
├── transform.py
├── load.py
├── main.py
├── fashion.ipynb
├── output_data.csv
└── README.md
```

## 📊 Dataset Information

**Dataset Name:** Fashion Retail Sales

**Input File:** `Fashion_Retail_Sales.csv`

The dataset contains fashion retail sales information, including:

- Customer Reference ID
- Item Purchased
- Purchase Amount (USD)
- Date Purchase
- Review Rating
- Payment Method

## ⚙️ ETL Process

The project consists of three major stages:

### 1. Extract

The extraction process reads the raw fashion retail sales dataset from a CSV file using Pandas.

**File:** `extract.py`

### 2. Transform

The transformation process performs the following operations:

- Renames the Purchase Amount column.
- Handles missing review ratings using the mean.
- Handles missing purchase amounts using the median.
- Converts purchase amounts into float format.
- Identifies outliers using the Interquartile Range (IQR) method.
- Caps values above the upper IQR fence.
- Encodes Item Purchased and Payment Method using Label Encoding.
- Extracts day, month, and year from purchase dates.
- Removes the original Date Purchase column.
- Standardizes purchase amounts using StandardScaler.

**File:** `transform.py`

### 3. Load

The loading process saves the transformed dataset into a new CSV file without including the DataFrame index.

**File:** `load.py`

## 🔄 ETL Workflow

```text
Raw Fashion Retail Sales Dataset
              |
              v
          EXTRACTION
              |
              v
       Data Transformation
              |
     ---------------------
     |         |         |
  Missing   Outlier   Encoding
  Values   Handling
     |         |         |
     ---------------------
              |
              v
       Feature Engineering
              |
              v
        Standardization
              |
              v
            LOADING
              |
              v
       output_data.csv
```

## 📦 Installation

Clone the repository:

```bash
git clone <your-repository-url>
```

Navigate to the project directory:

```bash
cd Fashion-Retail-Sales-ETL-Pipeline
```

Install the required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## ▶️ How to Run

Make sure the input CSV file is available in the working directory.

Execute the main Python file:

```bash
python main.py
```

The pipeline automatically performs extraction, transformation, and loading.

## 📁 Output

After successful execution, the processed dataset is saved as:

```text
output_data.csv
```

The output contains cleaned and transformed fashion retail sales data, including encoded categorical features, date-related features, and standardized purchase amounts.

## 💡 Key Learnings

- Understanding the ETL pipeline architecture.
- Working with real-world CSV datasets.
- Data cleaning and preprocessing using Pandas.
- Handling missing values and outliers.
- Categorical encoding techniques.
- Feature engineering and date extraction.
- Numerical data standardization.
- Building modular Python applications.

## 🚀 Future Improvements

- Automate ETL pipeline execution.
- Integrate a SQL database for data storage.
- Add data validation and error handling.
- Generate automated data quality reports.
- Build interactive dashboards for sales analysis.
- Schedule pipeline execution.

## 📝 Conclusion

The Fashion Retail Sales Data ETL Pipeline demonstrates how raw retail sales data can be converted into a clean and structured dataset through extraction, transformation, and loading. It provides practical experience in Python programming, data preprocessing, and fundamental data engineering concepts.

---

**Project Name:** Fashion Retail Sales Data ETL Pipeline

**Domain:** Data Engineering

**Programming Language:** Python
