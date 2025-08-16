
# 🧪 Certified Data Science Practitioner (CDSP) - ETL Lab

## Lab Objective
In this hands-on lab, you will perform a full **ETL (Extract, Transform, Load)** workflow using a real-world dataset of **consumer loan complaints**. You will:

- Load (Extract) data from a CSV file.
- Clean and format (Transform) the dataset for usability.
- Save (Load) the cleaned dataset for future analysis.

---

## 🗂 Dataset Overview

**File Path:**  
`/home/student/CDSP/ETL/data/consumer_loan_complaints.csv`

**Columns include:**
- `Date received` – Date of complaint submission
- `Product` – Financial product category
- `Issue` – Complaint type
- `State`, `ZIP code` – Location data
- `Company response to consumer` – Resolution status
- `Timely response?`, `Consumer disputed?` – Flags

---

## 📥 Step 1: Extract the Data

Load the CSV file into a pandas DataFrame:

```python
import pandas as pd

# Load the dataset
file_path = '/home/student/CDSP/ETL/data/consumer_loan_complaints.csv'
complaints_data = pd.read_csv(file_path)

# View the first 10 rows
complaints_data.head(10)
```

---

## 🛠️ Step 2: Transform the Data

### A. Explore the structure and check missing values

```python
complaints_data.info()
complaints_data.isnull().sum()
```

### B. Drop columns with too many missing values

```python
# Drop columns where more than 40% of data is missing
complaints_data = complaints_data.dropna(axis=1, thresh=len(complaints_data) * 0.6)
```

### C. Remove rows with missing values in key fields

```python
# Remove rows missing essential columns
complaints_data = complaints_data.dropna(subset=['Product', 'Issue', 'Company'])
```

### D. Convert date fields and extract features

```python
# Convert to datetime format
complaints_data['Date received'] = pd.to_datetime(complaints_data['Date received'], errors='coerce')

# Extract new features
complaints_data['Year'] = complaints_data['Date received'].dt.year
complaints_data['Month'] = complaints_data['Date received'].dt.month
```

### E. Standardize column names and text (Optional)

```python
# Clean column names
complaints_data.columns = [col.strip().lower().replace(" ", "_") for col in complaints_data.columns]

# Standardize 'product' values
complaints_data['product'] = complaints_data['product'].str.title()
```

---

## 💾 Step 3: Load the Cleaned Data

Save the cleaned dataset for future analysis.

```python
# Save the cleaned dataset
output_path = '/home/student/CDSP/ETL/data/cleaned_complaints.csv'
complaints_data.to_csv(output_path, index=False)

print(f"Cleaned data saved to {output_path}")
```

---

## ✅ Lab Complete

🎉 You have completed a real-world ETL cycle:

- Extracted data from a CSV file
- Transformed it with cleaning and feature engineering
- Loaded a cleaned dataset to disk

---

## 📈 Suggested Next Steps
- Perform exploratory data analysis (EDA)
- Create data visualizations using `matplotlib` or `seaborn`
- Begin feature selection and modeling

---
