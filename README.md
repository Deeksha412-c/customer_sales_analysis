# Customer Sales Analysis

## Project Overview
This project uses Python and Pandas to analyze sales performance and customer churn. It explores customer spending, regional revenue, monthly sales trends, product performance, and churn patterns to identify useful business insights.

## Objectives
- Clean and validate sales and customer datasets.
- Analyze customer spending and purchase metrics.
- Compare sales performance across regions and products.
- Identify monthly revenue trends.
- Examine customer churn by contract type and payment method.
- Create visualizations to communicate findings.

## Tools and Technologies
- Python
- Pandas
- Matplotlib
- Jupyter Notebook

## Project Structure
```text
customer_sales_analysis/
├── customer_analysis.ipynb
├── README.md
├── requirements.txt
├── data/
│   ├── sales_data.csv
│   ├── customer_data.csv
│   └── cleaned_sales_data.csv
├── visualizations/
├── report/
└── screenshots/
```

## Analysis Performed
1. Data loading and inspection
2. Missing-value and duplicate checks
3. Date conversion and text cleaning
4. Sales calculation validation
5. Customer spending analysis
6. Regional sales analysis
7. Monthly revenue analysis
8. Product performance analysis
9. Product-by-region pivot table
10. Customer churn analysis by contract and payment method
11. Data visualization

## Key Findings
- Total recorded sales revenue: 12,365,048.
- Total quantity sold: 478 units.
- Total sales records: 100.
- Unique customers in the sales dataset: 100.
- Highest-revenue month in the analyzed period: March 2024, with 4,485,006.
- Highest-revenue product: Laptop, with 3,889,210.
- Highest-revenue region: North, with 3,983,635.
- Customer churn rate in the separate customer dataset: 10.60%.
- Month-to-month contracts had the highest observed churn rate at 20.59%.
- Credit Card customers had the highest observed churn rate by payment method at 13.48%.

## Important Data Limitation
The sales dataset uses customer IDs such as `CUST016`, while the customer dataset uses IDs such as `C00001`. No customer IDs matched during validation. Therefore, the datasets were analyzed separately, and customer churn findings cannot be directly attributed to individual sales customers.

The sales dataset also contains no explicit order identifier, limiting analysis of products purchased together and repeat purchasing behavior.

## How to Run
1. Install Python.
2. Open a terminal in the project folder.
3. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

4. Open the notebook:

   ```bash
   jupyter notebook customer_analysis.ipynb
   ```

5. Run the notebook cells in order.

## Conclusion
This project demonstrates practical use of Pandas for data preparation, aggregation, pivot tables, and business analysis, along with Matplotlib for visualization. The findings highlight differences in product, regional, and customer churn performance while documenting important limitations in the available data.