# Retail Store Sales Data Cleaning with Pandas

## 📌 Project Overview
This project focuses on cleaning and preparing a retail store sales dataset using Python and Pandas in Google Colab. The goal was to improve data quality, handle missing values, perform basic exploratory data analysis, and prepare the dataset for visualization in Power BI.

## 🎯 Objectives
- Understand the structure and quality of retail sales data.
- Identify and handle missing values.
- Check for duplicate records and invalid values.
- Create useful columns for further analysis.
- Explore revenue patterns across product categories, items, and months.
- Prepare a cleaned dataset for Power BI.

## 🛠️ Tools & Technologies
- Python
- Pandas
- Google Colab
- Power BI (for planned visualization)

## 📂 Dataset
The dataset contains **12,575 rows and 11 columns**, covering retail transactions such as product categories, item names, prices, quantities, payment methods, transaction dates, and discount information.

## 🧹 Data Cleaning Process

### 1. Data Inspection
- Examined the first rows, dataset dimensions, column names, and data types.
- Identified missing values in important columns.

### 2. Missing Value Handling
- Created `Item Cleaned` to fill missing item names using observed relationships between product categories and prices.
- Created `Price Cleaned` to calculate missing prices where quantity and total spent were available.
- Preserved missing quantities, totals, and discount values when reliable information was unavailable.

### 3. Date and Feature Engineering
- Converted `Transaction Date` into a proper datetime format.
- Created a `Month` column for monthly analysis.
- Created a `Revenue` column using:

  `Revenue = Price Cleaned × Quantity`

### 4. Data Validation
- Checked for duplicate rows and duplicate transaction IDs.
- Checked for negative quantities and non-positive recorded totals.
- Verified that existing complete transaction totals matched price multiplied by quantity.

### 5. Data Export
- Prepared a final dataset using cleaned item names and prices.
- Exported the cleaned data to CSV for further analysis and visualization.

## 📊 Key Findings

- **Total calculated revenue:** 1,552,071 across rows with available revenue values.
- **Top revenue-generating category:** Butchers, with 208,118 in calculated revenue.
- **Lowest revenue-generating category:** Milk Products, with 180,112 in calculated revenue.
- **Missing item names after cleaning:** 0.
- **Missing prices after cleaning:** 0.
- **Duplicate rows found:** 0.
- **Duplicate transaction IDs found:** 0.

*Note: Revenue is calculated from available price and quantity values. The total is partial because 604 rows have missing quantities and therefore missing calculated revenue. January 2025 contains data only through January 18, so it represents a partial month.*

## ⚠️ Data Limitations
- 604 rows have missing quantities and recorded totals.
- 4,199 rows have unknown discount status.
- Some item names were inferred from observed category-price relationships, and some prices were calculated from available transaction values. These results may not independently confirm the original values.
- Missing values were retained when there was insufficient information to recover them reliably.

## 📁 Output
`Retail_Store_Sales_Cleaned.csv`

The exported dataset is intended for further analysis and dashboard development in Power BI.

## 📚 Key Learnings
Through this project, I practised:
- Inspecting datasets using Pandas.
- Identifying and handling missing values.
- Working with date and numeric columns.
- Creating calculated columns.
- Checking data quality and duplicates.
- Grouping and summarizing data to identify business patterns.
- Preparing data for visualization tools.

## 🚀 Next Steps
- Build an interactive Power BI dashboard.
- Visualize monthly revenue and category performance.
- Create KPI cards and top-item analysis.
- Explore payment methods and discount patterns while accounting for missing data.

---

**Project Type:** Data Cleaning & Exploratory Data Analysis  
**Level:** Beginner  
**Created using:** Python, Pandas, and Google Colab
