# Lawn Service Operations & Data Cleaning Analysis

This project provides a clean, business-oriented data analysis pipeline for a lawn service dataset consisting of 1,000 booking records across 2025 and 2026. The goal of this analysis is to transform raw operational data into actionable insights and prepare non-technical, stakeholder-friendly reports.

---

## 📌 Business Overview & Key Metrics

* **Total Bookings Analyzed:** 1,000 records
* **Timeframe:** 2025 (248 bookings) – 2026 (752 bookings)
* **Average Customer Rating:** **2.98 / 5.0**
* **Service Breakdown:**
  * **Hedge Trimming:** 353 bookings
  * **Lawn Mowing:** 345 bookings
  * **Weed Control:** 302 bookings
* **Booking Status Distribution:**
  * **Pending:** 335
  * **Completed:** 333
  * **Confirmed:** 332

---

## 🛠️ Data Cleaning & Missing Value Translation

Raw technical data often contains `NULL` or missing values that confuse non-technical teams and executives. Instead of dropping these rows or displaying cryptic system errors, missing values were translated into clear business terminology:

| Dataset Field | Missing Count | Technical State | Non-Technical Business Label | Business Reason |
| :--- | :--- | :--- | :--- | :--- |
| `zip_code` | 518 | `NaN` / `NULL` | **`Unspecified Location`** | Customer omitted postal code during booking. |
| `final_price` | 73 | `NaN` / `NULL` | **`Pending Billing`** | Service is in progress or unbilled; revenue is pending. |
| `duration_minutes` | 48 | `NaN` / `NULL` | **`Not Tracked`** | Field provider did not log clock-in/out duration. |
| `quoted_price` | 42 | `NaN` / `NULL` | **`Custom Estimate Required`** | Standard pricing was bypassed; requires manual review. |

---

## 📁 Repository Structure

* **`Lawn_org_ana_non_tech.ipynb`**: Interactive Jupyter Notebook containing the data exploration, missing value logic, and statistical summaries.
* **`README.md`**: Project overview and business metric documentation.

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git)
