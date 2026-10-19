# Customer Sales Analysis

## Project Overview

This project uses Python, Pandas, and Matplotlib to analyze sales performance and customer churn. It explores product performance, regional revenue, monthly sales trends, customer spending, and churn patterns to identify useful business insights.

This project was completed as part of a Week 5 data analysis internship task focused on advanced data manipulation with Pandas.

## Objectives

- Inspect, clean, and validate sales and customer datasets.
- Analyze recorded customer spending and sales metrics.
- Compare revenue across products and regions.
- Identify monthly revenue trends.
- Examine customer churn by contract type and payment method.
- Practise grouping, aggregation, conditional filtering, string operations, datetime extraction, merging, and pivot tables.
- Create visualizations to communicate findings.

## Tools and Technologies

- Python 3
- Pandas
- Matplotlib
- Jupyter Notebook
- CSV datasets

## Project Structure

```text
customer_sales_analysis/
├── customer_analysis.ipynb
├── README.md
├── requirements.txt
├── analysis_report.pdf
├── data/
│   ├── sales_data.csv
│   ├── customer_data.csv
│   └── cleaned_sales_data.csv
├── visualizations/
│   ├── monthly_revenue_trend.png
│   ├── product_revenue.png
│   ├── revenue_by_region.png
│   ├── churn_by_contract.png
│   ├── churn_by_payment_method.png
│   └── revenue_by_product_dashboard.png
├── report/
│   └── project_report.md
└── screenshots/
```

*Note: The structure above describes the intended project files. Confirm the filenames and include `analysis_report.pdf` and screenshots after creating them. Update the customer dataset filename if your actual file is named `customer_churn.csv`.*

## Analysis Performed

1. Data loading and inspection.
2. Missing-value and duplicate checks.
3. Date conversion and text cleaning.
4. Sales calculation validation.
5. Customer spending analysis.
6. Regional sales analysis.
7. Monthly revenue analysis.
8. Product performance analysis.
9. Conditional filtering using AND and OR.
10. String operations and datetime extraction.
11. Product-by-region pivot table.
12. Customer churn analysis by contract type and payment method.
13. Data visualization and summary reporting.

## Key Findings

- **Total recorded sales revenue:** 12,365,048.
- **Total quantity sold:** 478 units.
- **Total sales records:** 100.
- **Unique customer IDs in the sales dataset:** 100.
- **Highest-revenue month in the analyzed period:** March 2024, with 4,485,006.
- **Highest-revenue product:** Laptop, with 3,889,210.
- **Highest-revenue region:** North, with 3,983,635.
- **Overall churn rate in the separate customer dataset:** 10.60%.
- **Highest observed churn by contract:** Month-to-month, at 20.59%.
- **Highest observed churn by payment method:** Credit Card, at 13.48%.

These are descriptive findings from the available datasets; they do not establish causal relationships.

## Important Data Limitations

The sales dataset uses customer IDs such as `CUST016`, while the customer dataset uses IDs such as `C00001`. No customer IDs matched during validation. Therefore, the datasets were analyzed separately, and churn findings cannot be directly attributed to individual sales customers.

The sales dataset also has no explicit order identifier. Consequently, repeat purchasing, customer lifetime value, and products purchased together cannot be reliably established from the available sales records.

## Setup and Execution

### 1. Install Python

Install Python 3 from [python.org](https://www.python.org/downloads/).

### 2. Open the project folder

Open a terminal in the `customer_sales_analysis` directory.

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```bash
jupyter notebook customer_analysis.ipynb
```

Run the notebook cells in order.

## Report and Visualizations

- The project report is provided as `analysis_report.pdf` after the PDF has been generated.
- The `visualizations/` directory contains the sales and churn charts.
- The `screenshots/` directory contains screenshots of actual notebook execution and analysis outputs once captured.

## Conclusion

This project demonstrates practical use of Pandas for data preparation, conditional filtering, aggregation, pivot tables, and exploratory analysis, together with Matplotlib for visualization. The results highlight differences in product, regional, and customer churn performance while documenting limitations in the available data.
