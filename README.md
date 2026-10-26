# Retail Store Sales Data Cleaning with Python

## About the Project
In this project, I cleaned and explored a retail store sales dataset using Python and Pandas in Google Colab. The main goal was to fix data quality issues and prepare the data for business analysis and Power BI.

## Steps I Followed

1. **Uploaded the Dataset**  
   Loaded the CSV file using Pandas.

2. **Inspected the Data**  
   Checked the first few rows, number of rows and columns, column names, data types, and basic statistics using `head()`, `shape`, `info()`, and `describe()`.

3. **Checked Missing Values**  
   Found missing values in item names, prices, quantities, total spent, and discount information.

4. **Analysed Discount Data**  
   Checked whether missing discounts could be understood using categories, payment methods, and spending patterns. Since no reliable pattern was found, I left the missing values unchanged.

5. **Cleaned Item Names**  
   Used existing category and price patterns to fill missing item names where possible. These names are inferred and may not always be exact.

6. **Filled Missing Prices**  
   Calculated missing prices using `Total Spent ÷ Quantity` wherever the required values were available.

7. **Handled Remaining Missing Values**  
   Left missing quantities and total spent values unchanged because there was not enough information to calculate them reliably.

8. **Checked Data Quality**  
   Checked for duplicate rows, duplicate transaction IDs, negative quantities, and non-positive total values. No issues were found in these checks.

9. **Created New Columns**  
   Created a `Month` column from the transaction date and a `Revenue` column using price per unit multiplied by quantity.

10. **Analysed Sales**  
    Compared revenue across product categories, individual items, and months to identify sales patterns.

11. **Exported the Cleaned Data**  
    Prepared the cleaned dataset as a CSV file for further analysis and Power BI visualisation.

## Key Findings

- The original dataset contained **12,575 rows and 11 columns**.
- **Butchers** had the highest total revenue among the product categories.
- **Milk Products** had the lowest total revenue among the product categories.
- Missing discount information could not be reliably inferred, so it was left unchanged.
- Some quantity and total spent values remained missing because they could not be calculated reliably.

## Tools Used

- Python
- Pandas
- Google Colab

## Output

`Retail_Store_Sales_Cleaned.csv`

The cleaned dataset can be used to create a Power BI dashboard and explore sales performance.

## What I Learned

- How to inspect a dataset using Pandas.
- How to identify and handle missing values.
- How to investigate data patterns before filling missing information.
- How to check duplicates and validate data quality.
- How to create new columns for analysis.
- How to find useful business insights from sales data.

## Note

Some item names were inferred using existing data patterns. Missing values that could not be calculated reliably were left unchanged rather than filled with guesses.


**Project Type:** Data Cleaning & Exploratory Data Analysis    
**Created using:** Python, Pandas, and Google Colab
