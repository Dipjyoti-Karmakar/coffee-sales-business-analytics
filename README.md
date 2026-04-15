# Coffee Sales Business Analytics

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

## Project Overview
This project analyzes sales and customer data for a coffee retail chain. Using **Python**, raw transaction logs are cleaned, transformed, and explored to uncover trends in customer behavior, product performance, and payment preferences.

The analysis is performed in a Jupyter Notebook, using **Pandas** for data manipulation and **Matplotlib/Seaborn** for visualization.

## Objectives
* **Data Preparation:** Handling missing values, correcting data types, and combining datasets.
* **Exploratory Data Analysis (EDA):** Identifying patterns in sales, peak hours, and customer segments.
* **Cross-Month Comparison:** Comparing February and March data for growth trends and behavioral shifts.
* **Product Analysis:** Determining which coffees drive the most revenue.

## Data Description
The analysis uses two datasets combined for a holistic view:

* **`transactions.csv`** - Transaction-level sales data including datetime, card ID, coffee name, payment type, and amount.
* **`customer_details.csv`** - Additional customer transaction records with datetime, coffee name, payment type, and amount.

## Project Structure

```
root/
├── data/
│   └── raw/              ← Original, untouched source files (.csv, .xlsx, .json)
├── notebooks/
│   └── eda/              ← Exploratory data analysis (e.g., 01_coffee_sales_analytics.ipynb)
├── .gitignore            ← Git ignore definitions
├── requirements.txt      ← Python package dependencies
└── README.md             ← Top-level documentation
```

## Tech Stack
* **Language:** Python
* **Libraries:**
    * `Pandas` & `NumPy` (Data Manipulation)
    * `Matplotlib` & `Seaborn` (Data Visualization)
    * `Jupyter Notebook` (Interactive Development Environment)

## Key Insights & Analysis
The notebook explores the following business questions:

**A. Customer Behavior**
- Most popular coffees (Americano with Milk leads)
- Payment preferences (Card over Cash)
- Peak purchase hours (6 PM is busiest)

**B. Sales Analysis**
- Top revenue-earning coffee (Latte)
- Average ticket size per coffee
- Daily sales trends over time

**C. Operational Insights**
- Peak transaction hours for staffing decisions
- Repeat customers identified by card usage
- February vs. March behavioral differences

**D. Cross-Month Comparison**
- Monthly growth trends
- Payment preference changes
- Coffee-wise month-over-month sales comparison

## Quantitative Findings (From Notebook Outputs)
- Total analyzed transactions (combined): 3,898
- Payment method split: Card 3,729 (95.66%), Cash 169 (4.34%)
- Top 5 coffees by purchase count:
    - Americano with Milk: 824
    - Latte: 806
    - Americano: 593
    - Cappuccino: 517
    - Cortado: 292
- Top revenue coffee: Latte with total revenue of 28,658.3
- Peak purchase hour: 18:00 with 113 transactions
- Repeat-customer signal: 545 unique cards made more than one purchase
- Highest repeat card activity: ANON-0000-0000-0012 with 129 purchases
- Month comparison (source datasets):
    - February 2025 total revenue: 16,804.48
    - March 2025 total revenue: 13,287.44
    - Revenue growth from February to March: -20.93%
    - *Note: Figures corrected after fixing aggregation bug where the entire historical dataset was mistakenly treated as February data. Verified on April 15, 2026.*

## How to Run
1.  **Clone the Repository:**
    ```bash
    # Clone the repository (HTTPS - recommended)
    git clone https://github.com/Dipjyoti-Karmakar/coffee-sales-business-analytics.git

    # Or using SSH (for contributors with SSH keys)
    git clone git@github.com:Dipjyoti-Karmakar/coffee-sales-business-analytics.git
    ```
2.  **Set up the Environment:**
    ```bash
    # Create and activate virtual environment
    python -m venv venv
    
    # On Windows (Command Prompt):
    venv\Scripts\activate
    # On Windows (PowerShell):
    .\venv\Scripts\Activate.ps1

    # Install dependencies
    pip install pandas numpy matplotlib seaborn jupyter
    ```
3.  **Run the Analysis:**
    Open `notebooks/eda/01_coffee_sales_analytics.ipynb` in Jupyter Notebook or VS Code. Ensure that `customer_details.csv` and `transactions.csv` are in the `data/raw/` directory.

## Author
**Dipjyoti Karmakar**
* **Role:** Data Analyst / Business Intelligence
* **Connect with me:** [LinkedIn Profile](https://www.linkedin.com/in/dipjyoti-karmakar-91050a37a)

---
*This project is part of my portfolio demonstrating skills in Data Cleaning, EDA, and Python-based Analytics.*
