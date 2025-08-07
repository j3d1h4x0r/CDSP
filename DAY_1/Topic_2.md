🔧 Topic 2: Extract, Transform, and Load (ETL) Data

This topic introduces the core data engineering workflow used in every data science project: ETL.

🔄 ETL Overview

ETL stands for:

Extract: Pulling data from various sources

Transform: Cleaning, reshaping, and preparing data

Load: Storing data for modeling or analysis

ETL ensures that your models and analytics work with clean, structured, and usable data.

📀 1. Extracting Data

📊 Types of Data

Structured: Tables, databases (SQL, CSV, Excel)

Unstructured: Images, audio, PDFs, social media posts

Semi-structured: JSON, XML

🤝 Common Data Sources

CSV/Excel files

SQL/NoSQL databases

APIs (e.g., RESTful APIs)

Cloud storage (S3, Azure Blob, Google Cloud)

Web scraping (HTML parsing)

🤖 First-Party vs Third-Party Data

First-party: Owned by the organization

Second-party: Shared partner data

Third-party: External datasets (e.g., Kaggle, AWS, public APIs)

🧰 Open Datasets

Popular sources:

Kaggle: https://www.kaggle.com/datasets

UCI ML Repository: https://archive.ics.uci.edu/ml

Data.gov (US), Data.gov.uk, Data.gov.in

🔒 Data Access Practices

Use read-only permissions

Secure API keys and tokens

Minimize extracted columns

Anonymize PII early

⚙️ Practical Tip:

Use tools like pandas.read_csv(), requests.get(), and SQLAlchemy to extract and preview datasets in Python.

🔹 Use Case:

A telecom company pulls user transaction records from PostgreSQL and merges them with marketing data in CSV format.

💡 2. Transforming Data

🌀 Data Cleaning Tasks

Remove duplicates

Handle missing values

Fix data types

Format dates

Normalize units (e.g., lbs → kg)

🏛 Data Structuring

Merge/join multiple tables

Pivot/unpivot data

Aggregate rows (e.g., transaction totals per user)

⚖️ Feature Types

Quantitative: Numerical (e.g., income)

Qualitative: Categorical (e.g., gender)

Ordinal: Ranked categories (e.g., education level)

↔️ Continuous vs Discrete

Continuous: Infinite values (e.g., height)

Discrete: Countable (e.g., number of purchases)

🤷 Common Python Libraries

pandas: For all tabular data operations

numpy: Numeric transformations

datetime: Time-related parsing

🔹 Use Case:

A bank has transaction data in seconds. To analyze call durations, durations are aggregated into minutes and then grouped by customer.

✅ Governance Considerations:

Document all transformations

Ensure data security during transformation

Anonymize before joining or exporting

🛠️ 3. Loading Data

📂 Load Destinations

SQL databases

Data warehouses (e.g., Snowflake, BigQuery)

Dashboards (e.g., Tableau, Power BI)

Files (CSV, JSON, Parquet)

↔️ Merging & Joining

Inner Join: Only matching rows

Left Join: All from left, matched from right

Right Join: All from right, matched from left

Outer Join: All from both, matched or not

💡 Practical Tips

Avoid full refresh unless necessary

Use incremental loads for large datasets

Track data versions

🔹 Use Case:

After cleaning and combining transaction and user data, the final DataFrame is exported to a PostgreSQL database for dashboard reporting.

🗋 ETL Checklist



📊 Summary

ETL is the backbone of practical data science. Clean, well-prepared data leads to better models, faster iteration, and stronger business impact.

“Garbage in, garbage out.” — Every Data Scientist Eve
