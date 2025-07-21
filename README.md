# Fraud Detection Dashboard (Commonwealth Bank Virtual Experience)

![Status](https://img.shields.io/badge/Status-Completed-green)
![Platform](https://img.shields.io/badge/Platform-Splunk%20Cloud-blue)
![Dataset](https://img.shields.io/badge/Dataset-Prepared_Data.csv-orange)

## 📌 Project Overview
This project was completed as part of the **Commonwealth Bank Cybersecurity Virtual Experience Program** on Forage. It simulates real-world fraud detection scenarios using Splunk for data visualization and analysis.

## ✅ Objectives
- Import financial transaction data into Splunk
- Build SPL queries for fraud detection
- Visualize trends in fraudulent activities by:
  - Transaction category
  - Customer age group
  - Gender
  - Merchant

## 🛠 Tech Stack
- Splunk Cloud
- SPL (Search Processing Language)
- CSV Dataset (Simulated)

## 🔍 SPL Queries Used
```spl
source="prepared_data.csv" | top category
source="prepared_data.csv" fraud=1 | stats count by age category step gender
source="prepared_data.csv" fraud=1 | stats count by gender category
source="prepared_data.csv" fraud=1 | stats count by age merchant
