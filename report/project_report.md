# Customer Sales Analysis — Project Report

## 1. Introduction

This project analyzes sales and customer data using Python, Pandas, and Matplotlib. The objective is to identify business insights from sales transactions, product performance, regional revenue, monthly trends, and customer churn.

## 2. Objectives

- Inspect and clean the available datasets.
- Validate sales calculations and data consistency.
- Identify high-spending customers.
- Compare revenue across products and regions.
- Analyze monthly revenue trends.
- Calculate customer churn rates by contract type and payment method.
- Present findings using visualizations.

## 3. Tools and Technologies

- **Programming language:** Python
- **Data analysis:** Pandas
- **Data visualization:** Matplotlib
- **Development environment:** Jupyter Notebook
- **Data format:** CSV

## 4. Datasets

### Sales dataset
The sales dataset contains 100 records and seven original columns: Date, Product, Quantity, Price, Customer_ID, Region, and Total_Sales.

### Customer dataset
The customer dataset contains 500 customer records and nine columns, including Tenure, MonthlyCharges, TotalCharges, Contract, PaymentMethod, and Churn.

## 5. Data Cleaning and Validation

The following steps were performed:

- Inspected dataset dimensions, columns, and data types.
- Checked for missing values and duplicate records.
- Converted the sales Date column to a datetime type.
- Removed leading and trailing spaces from selected text columns.
- Checked numeric fields for invalid values.
- Verified that Total_Sales equals Quantity multiplied by Price.
- Added Year, Month, Day, and Year_Month columns for time-based analysis.

The sales calculation validation found 100 matching records and zero mismatches.

## 6. Analysis and Results

### 6.1 Overall Sales Performance

| Metric | Result |
|---|---:|
| Total revenue | 12,365,048.00 |
| Total quantity sold | 478 |
| Sales records | 100 |
| Unique sales customers | 100 |
| Average sale value per record | 123,650.48 |

### 6.2 Customer Spending

Customers were ranked by total recorded spending. CUST016 ranked first with total recorded spending of 373,932.

Every customer appeared once in the sales dataset, so this analysis identifies high-value recorded sales rather than repeat purchasing or lifetime customer value.

### 6.3 Regional Sales Analysis

| Region | Total Revenue | Quantity Sold | Sales Records |
|---|---:|---:|---:|
| North | 3,983,635 | 147 | 28 |
| South | 3,737,852 | 143 | 27 |
| East | 2,519,639 | 94 | 19 |
| West | 2,123,922 | 94 | 26 |

North generated the highest revenue, while West generated the lowest. West had more sales records than East but lower total revenue, indicating a difference in average recorded sales value.

### 6.4 Monthly Revenue Analysis

| Month | Total Revenue |
|---|---:|
| January 2024 | 4,120,524 |
| February 2024 | 2,656,050 |
| March 2024 | 4,485,006 |
| April 2024 | 1,103,468 |

March generated the highest revenue during the analyzed period. April generated the lowest revenue. The available date coverage should be checked before interpreting April as a complete month.

### 6.5 Product Performance

| Product | Total Revenue | Units Sold | Sales Records |
|---|---:|---:|---:|
| Laptop | 3,889,210 | 136 | 24 |
| Tablet | 2,884,340 | 127 | 26 |
| Phone | 2,859,394 | 101 | 20 |
| Headphones | 1,384,033 | 48 | 15 |
| Monitor | 1,348,071 | 66 | 15 |

Laptop generated the highest revenue and had the highest number of units sold. Tablet had the most sales records. Monitor generated the lowest revenue.

### 6.6 Customer Churn Analysis

The customer dataset contained 500 records, of which 53 were marked as churned.

**Overall churn rate: 10.60%.**

#### Churn by contract type

| Contract | Customers | Churned | Churn Rate |
|---|---:|---:|---:|
| Month-to-month | 170 | 35 | 20.59% |
| Two year | 144 | 10 | 6.94% |
| One year | 186 | 8 | 4.30% |

Month-to-month customers had the highest observed churn rate.

#### Churn by payment method

| Payment Method | Customers | Churned | Churn Rate |
|---|---:|---:|---:|
| Credit Card | 178 | 24 | 13.48% |
| Electronic Check | 163 | 18 | 11.04% |
| Bank Transfer | 159 | 11 | 6.92% |

Credit Card customers had the highest observed churn rate among the listed payment methods. These patterns show associations and do not establish that contract type or payment method causes churn.

## 7. Visualizations

The project includes charts for:

- Monthly revenue trends
- Product revenue
- Revenue by region
- Customer churn by contract type
- Customer churn by payment method
- Product revenue dashboard comparison

## 8. Business Recommendations

1. Review laptop inventory and availability because laptops generated the highest revenue.
2. Investigate regional differences in revenue, particularly the lower recorded revenue in the West.
3. Examine the reasons for higher churn among month-to-month customers and test appropriate retention initiatives.
4. Investigate churn differences across payment methods without assuming payment method is the cause.
5. Collect compatible customer identifiers and order IDs in future datasets to enable reliable customer-level joins, repeat-purchase analysis, and product-combination analysis.

## 9. Data Limitations

The sales dataset uses customer IDs such as `CUST016`, while the customer dataset uses IDs such as `C00001`. No customer IDs matched during validation. The datasets were therefore analyzed separately, and churn results cannot be linked to individual sales customers.

The sales dataset has no explicit order identifier. Consequently, repeat purchases and products bought together cannot be reliably established.

## 10. Conclusion

This project demonstrates practical data analysis using Pandas and Matplotlib. Data validation, aggregation, pivot tables, churn-rate calculations, and visualizations were used to summarize sales performance and identify customer-retention patterns. The findings provide useful starting points for business investigation while recognizing limitations in the available data.