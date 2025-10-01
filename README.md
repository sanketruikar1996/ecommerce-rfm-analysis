# E-commerce RFM Analysis

## Project Overview
This project demonstrates **RFM (Recency, Frequency, Monetary) analysis** on an online retail dataset using PySpark on Databricks.  
The goal is to segment customers based on their purchasing behavior, which helps businesses prioritize retention strategies, loyalty programs, and targeted marketing campaigns.

---

## Dataset
- Source: Online Retail Dataset  
- Features include:  
  - `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`  

---

## Data Cleaning & Transformation
- Handled missing values and replaced `Description` with "Unknown" where missing  
- Dropped rows without `CustomerID`  
- Removed negative quantities and duplicate rows  
- Adjusted schema for consistency (`CustomerID` as string)  

---

## RFM Analysis Steps
1. **Recency** – Days since the last purchase for each customer  
2. **Frequency** – Number of transactions per customer  
3. **Monetary** – Total revenue per customer  

**Implementation:**  
- Calculated Recency, Frequency, and Monetary values  
- Assigned scores (1–5) for each metric  
- Created a combined **RFM Segment** (`R_Score-F_Score-M_Score`) for each customer  

---

## Example Output
| CustomerID | Recency | Frequency | Monetary | RFM Segment |
|------------|---------|-----------|---------|-------------|
| 13256      | 14      | 1         | 0.0     | 4-1-1       |
| 16738      | 297     | 1         | 3.75    | 1-1-1       |
| 14792      | 63      | 2         | 6.2     | 3-1-1       |

---

## Future Work
- **Visualization**: Create bar charts or dashboards for RFM segments (Power BI / Databricks SQL)  
- **Segmentation**: Use clustering algorithms (KMeans) to group customers into actionable segments  
- **Pipeline Automation**: Wrap analysis in a Databricks notebook workflow or Airflow DAG for repeatable execution  

---

## Technologies Used
- Python, PySpark  
- Databricks  
- CSV / Parquet for data storage  

---

## How to Run
1. Clone the repository  
2. Open the notebook in Databricks  
3. Run all cells to reproduce RFM analysis  
4. Inspect `rfm_df` for the final output

---

## Key Takeaways
- Learned to perform end-to-end **data cleaning, transformation, and analytics**  
- Gained experience in **customer segmentation** using RFM scoring  
- Demonstrated ability to prepare datasets for **production-ready analysis**
