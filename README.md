````markdown
# Vendor Performance Data Analytics Case Study

## 📌 Project Overview

This project is an end-to-end data analytics solution designed to evaluate vendor performance for a retail business. By integrating **SQL, Python, and Power BI**, the project identifies which suppliers are driving profitability and which are contributing to **frozen capital** through unsold inventory.

The objective is to transform raw transactional data into **actionable business insights** that support smarter purchasing decisions, inventory optimization, and vendor negotiations.

---

## 🛠️ Tech Stack & Project Structure

- **Database**: SQLite used as the central data warehouse (`inventory.db`) to manage large-scale datasets beyond Excel’s capacity.
- **Data Ingestion (`ingestion_db.py`)**: Python + SQLAlchemy with batch processing (100,000 rows per batch) to efficiently load 1.5GB+ CSV files from Kaggle.
- **Data Engineering (`get_vendor_summary.py`)**: SQL CTEs (Common Table Expressions) used to combine Purchase, Sales, and Freight data into a unified analytical table.
- **Analysis (`Vendor Performance Analysis.ipynb`)**: Exploratory Data Analysis (EDA) and hypothesis testing to validate key business assumptions.
- **Visualization**: Interactive Power BI dashboard for executive-level reporting.

---

## 📊 Key Business Insights

- **The Margin Paradox**:  
  Statistical testing (Two-Sample T-Test) showed that **low-volume vendors achieve significantly higher profit margins (~41%)** compared to high-volume vendors (~31%).

- **Inventory Efficiency**:  
  Identified the **top 10 vendors with the highest unsold inventory value**, highlighting opportunities for stock clearance and capital recovery.

- **Bulk Purchasing Impact**:  
  Boxplot analysis used to assess whether larger purchase quantities consistently reduced unit purchase prices across key brands.

---

## 📸 Power BI Dashboard

Here’s a snapshot of the interactive dashboard showcasing vendor performance insights:

<p align="center">
  <img src="https://github.com/user-attachments/assets/eed44e0d-5568-4071-b423-31556bc460af" width="900" alt="Vendor Performance Dashboard">
</p>

---

## 🚀 How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/Vendor-Performance-Analysis.git
````

2. Download the dataset from **Kaggle** and place the CSV files inside the `/data` folder.

3. Run the ingestion script to build the SQLite database:

   ```bash
   python ingestion_db.py
   ```

4. Generate the vendor summary table:

   ```bash
   python get_vendor_summary.py
   ```

5. Load the `vendor_sales_summary` table into **Power BI** to explore the dashboard.

---

## 🙏 Credits & References

This project was inspired by and adapted from a data analytics case study tutorial by **Tech Classes**.

* Tutorial: Vendor Performance Analysis Case Study – Tech Classes
  [Watch on YouTube](https://youtu.be/nmCfNHjfgEY?si=k06EdA45jFrM8uvw)

All data engineering, analysis logic, and insights were implemented independently as part of a personal learning and portfolio project.

---

```
```
