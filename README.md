# Retail Sales & Customer Behavior Analysis

## Project Overview
This project analyzes retail transaction data to better understand customer purchasing behavior and retention trends over time.

Using Python and cohort analysis techniques, customers were grouped based on their first purchase month, and a retention matrix was created to measure how customer engagement changes across subsequent months.

### Key Findings
The following heatmap illustrates customer retention patterns based on cohort analysis. It provides a clear view of customer behavior and drop-off rates over time:

![Customer Retention Heatmap](Convert retention to precentage.jpg)

*Key Insight:* The analysis highlights that the most significant churn occurs after the first month, indicating a critical window for re-engagement strategies.

## Objectives
- Clean and prepare raw retail transaction data
- Perform feature engineering for customer behavior analysis
- Build customer cohorts based on first purchase month
- Calculate monthly retention rates
- Visualize retention patterns using a heatmap

## Tools & Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset
The dataset contains transactional retail data including:
- Invoice information
- Product details
- Quantity
- Price
- Customer IDs
- Country
- Invoice dates

## Data Cleaning Steps
- Removed missing `CustomerID` values
- Excluded canceled transactions
- Filtered out invalid records with non-positive quantity or unit price
- Converted `InvoiceDate` to datetime format

## Feature Engineering
The following features were created:
- `TotalPrice` = Quantity × UnitPrice
- `InvoiceMonth`
- `CohortMonth`
- `CohortIndex`

## Cohort Analysis
Customers were assigned to cohorts based on the month of their first purchase.  
A retention matrix was then created to track how many customers returned in each following month.

## Key Output
### Customer Retention Heatmap
![Retention Heatmap](images/retention_heatmap.png)

## Key Insights
- The highest customer count appears in the first month of each cohort.
- Retention decreases over time, which is a common pattern in retail behavior.
- Cohort analysis helps identify when customer drop-off is strongest.
- This analysis can support retention strategy and customer lifecycle planning.

## Files
- `notebooks/retail_sales_customer_behavior_cohort_analysis.ipynb` → full notebook
- `data/processed/online_retail_cleaned_with_cohort.csv` → cleaned dataset with cohort features
- `images/retention_heatmap.png` → retention visualization

## How to Run
1. Clone this repository
2. Install dependencies:
```bash
   pip install -r requirements.txt
   
