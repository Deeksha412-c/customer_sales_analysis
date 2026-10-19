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

### 5.1 Advanced Pandas Operations

Several Pandas operations were used to explore, transform, and summarize the datasets.

**Grouping and Aggregation**

The `groupby()` method was used to group sales records by product and region. Aggregation functions such as `sum()`, `mean()`, and `count()` calculated total revenue, average recorded sale value, and the number of sales records.

**Conditional Filtering**

Boolean conditions were used to filter records based on multiple criteria. The `&` operator combined conditions using AND, while the `|` operator combined conditions using OR. For example, sales from the North region with prices above the overall average were selected for further examination.

**String Operations**

Pandas string methods, including `str.strip()`, `str.title()`, and `str.contains()`, were used to standardize text values and identify product-specific records.

**Datetime Extraction**

The sales date column was converted to datetime format. The year, month, day, and year-month period were extracted to support time-based analysis.

**Merging and Joining**

A left merge was attempted between the sales and customer datasets using their customer ID columns. The merge returned no matching customer IDs. The datasets were therefore analyzed separately to avoid making unsupported customer-level conclusions.

**Pivot Tables**

A pivot table summarized total sales revenue by product and region. Row and column totals made it easier to compare product performance across regions.

These operations demonstrate practical use of Pandas for data preparation, filtering, aggregation, and exploratory analysis.

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

## 7.1 Testing and Validation

The project was tested using the available sales and customer datasets to check data quality, calculations, and analysis outputs.

### Data Quality Checks

- Checked dataset dimensions, column names, and data types.
- Verified that the sales dataset contained 100 records and the customer dataset contained 500 records.
- Checked both datasets for missing values and duplicate records.
- Checked for invalid sales dates. No invalid dates were found.
- Compared `Total_Sales` with `Quantity × Price`. All 100 sales records matched the expected calculation.

### Analysis Checks

- Verified product and regional revenue totals using grouping and aggregation.
- Confirmed that the pivot table totals matched the overall sales revenue of 12,365,048.
- Tested conditional filtering using AND and OR operators.
- Tested string operations for product identification and text standardization.
- Extracted year, month, and day from the sales dates.
- Attempted a customer-level merge and confirmed that no customer IDs matched across the two datasets.

### Validation Outcome

The main sales calculations and aggregation results were consistent across the analysis outputs. The customer merge limitation was identified and documented rather than forcing an invalid match. Customer churn statistics were therefore calculated independently from the sales analysis.

The results support the descriptive findings presented in this report. They do not establish causal relationships or predict future customer behavior.

## 7.2 Screenshot Documentation

Screenshots are included to demonstrate the execution of the notebook, data validation, analysis outputs, and visualizations.

The following screenshots should be included in the project submission:

1. **Data Loading and Inspection:** Shows the sales and customer datasets being loaded and their dimensions and column names being displayed.
2. **Data Cleaning and Validation:** Shows the data quality checks and sales calculation validation results.
3. **Pandas Analysis:** Shows the grouping, conditional filtering, datetime extraction, or pivot table output.
4. **Sales Dashboard and Visualizations:** Shows the generated charts for monthly revenue, product performance, regional revenue, and customer churn.

Screenshots should be captured from actual notebook executions and saved in the project's `screenshots/` directory. Each image should be clear, readable, and relevant to the corresponding analysis step.

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