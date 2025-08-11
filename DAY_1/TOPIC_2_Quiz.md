# **CDSP – Topic 2 Complex Scenario-Based Quiz**

### **Instructions**

-   Read each scenario carefully.
    
-   Choose the  **most appropriate answer(s)**  — some are multi-select.
    
-   Apply  **ETL best practices**,  **data governance**, and  **real-world problem-solving**.
    

----------

## **Scenario 1: The Government Health Data Project**

**Background:**  
A public health agency wants to analyze  **real-time COVID-19 case data**  from:

-   National hospital database (SQL, updated nightly)
    
-   State-level JSON API (updates every hour, but with occasional downtime)
    
-   CSV uploads from smaller clinics (manual, weekly)
    

They need insights  **every morning at 8 AM**  for decision-making.

----------

**Q1:**  
Which TWO extraction strategies best ensure  **timely**  and  **reliable**  access to the data?

-   A. Schedule automated SQL queries to run nightly and fetch data from the national database.
    
-   B. Poll the state-level API every 15 minutes and cache the results to handle downtime.
    
-   C. Replace the CSV uploads with live FTP feeds from clinics.
    
-   D. Only rely on the CSV data because it is manually verified and clean.
    

----------

**Q2:**  
While testing, you notice the JSON API sometimes returns incomplete data. Which  **ETL principle**  should guide your next step?

-   A. Apply schema validation during transformation to catch and log incomplete API responses.
    
-   B. Skip incomplete records entirely to avoid errors in loading.
    
-   C. Contact the API provider and wait for a permanent fix before proceeding.
    
-   D. Merge the API data with SQL and CSV sources during transformation to fill gaps.
    

----------

## **Scenario 2: The Global Retail Expansion**

**Background:**  
_ShopMax_  is consolidating sales data from:

-   US branch (CSV files with  `MM/DD/YYYY`  date format, USD currency)
    
-   UK branch (Excel with  `DD/MM/YYYY`, GBP currency)
    
-   Japan branch (JSON with Unix timestamps, JPY currency)
    

They plan to load all sales into a central PostgreSQL database for analytics.

----------

**Q3:**  
Which THREE transformation steps are critical before loading the data?

-   A. Standardize all date formats to ISO 8601 (`YYYY-MM-DD`).
    
-   B. Convert all currencies into a common standard (e.g., USD).
    
-   C. Change all product IDs to sequential integers for simplicity.
    
-   D. Normalize timestamp fields from Unix to human-readable dates.
    
-   E. Translate all product descriptions into English before loading.
    

----------

**Q4:**  
If the Japanese branch’s JSON files are  **nested objects**, which transformation action is required for compatibility with PostgreSQL?

-   A. Flatten nested JSON structures into relational tables.
    
-   B. Keep the JSON as-is and store it in a JSONB column.
    
-   C. Export the JSON to CSV without processing.
    
-   D. Delete the nested fields to simplify the schema.
    

----------

## **Scenario 3: The IoT Sensor Network**

**Background:**  
A smart agriculture company gathers:

-   Temperature & humidity data every 5 seconds from IoT sensors (MQTT stream)
    
-   Drone imagery once a day (large JPEG files)
    
-   Weather forecasts from a third-party API (JSON, hourly)
    

They must integrate all this into a  **data lake**.

----------

**Q5:**  
Which TWO  **loading strategies**  best handle this mix of high-frequency small data and large batch files?

-   A. Use a streaming pipeline (e.g., Kafka) for sensor data and batch ingestion for drone images.
    
-   B. Convert drone images into thumbnails before loading to save storage space.
    
-   C. Store sensor data in a time-series database and images in object storage linked via metadata.
    
-   D. Append all data into a single CSV file for simplicity.
    

----------

**Q6:**  
The weather API sometimes changes its field names without notice. Which transformation safeguard would  **most reduce pipeline failures**?

-   A. Implement schema mapping that automatically updates based on API documentation.
    
-   B. Build a transformation script that ignores unrecognized fields and logs anomalies.
    
-   C. Store raw API responses in a staging area before transformation.
    
-   D. Switch to a competitor’s API to avoid the problem entirely.
