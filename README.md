# mannatgill_bitsom_ba_2507628_part1_data_cleaning
# Part 1: Business Data Cleaning, Validation & Excel Reporting

## Repository Information

Repository Name:

mannatgill_2507628_part1_data_cleaning

## Problem Summary

A retail company exported order-level sales data from multiple internal systems. The raw dataset contained data quality issues including inconsistent text formatting, missing values, invalid discounts, date inconsistencies, shipping issues, and calculation mismatches.

The objective was to clean and validate the dataset, apply business rules, generate calculated fields, and create management-ready reports using Excel.

---

## Dataset Description

File Used:

* raw_orders.xlsx

The dataset contains:

* Order information
* Customer information
* Product information
* Sales information
* Shipping information
* Payment information

---

## Tools Used

* Microsoft Excel
* Pivot Tables
* Excel Formulas
* Data Validation
* Conditional Formatting

---

## Cleaning Steps Performed

### Text Standardization

The following fields were cleaned:

* customer_name
* segment
* region
* state
* city
* category
* sub_category
* ship_mode
* payment_status
* order_status

Actions performed:

* Removed leading spaces
* Removed trailing spaces
* Removed double spaces
* Standardized capitalization
* Standardized category names
* Standardized shipping mode values

### Date Cleaning

Fields cleaned:

* order_date
* ship_date

Actions performed:

* Converted to standard date format
* Validated missing dates
* Flagged invalid dates
* Flagged ship dates occurring before order dates

### Missing Value Handling

* Missing Region → Unknown
* Missing Ship Mode → Unknown
* Missing Discount → 0 (when valid)

### Discount Validation

Validated:

* Negative discounts
* Excessive discounts
* Text-based percentage values

### Duplicate Validation

Checked:

* Exact duplicate rows
* Duplicate Order IDs
* Conflicting duplicate records

---

## Business Rules Applied

1. Missing Region = Unknown
2. Missing Ship Mode = Unknown
3. Missing Discount = 0 when other sales fields are valid
4. Negative Discount = Invalid
5. Excessive Discount = Invalid
6. Ship Date before Order Date = Invalid
7. Cancelled Orders excluded from completed sales summaries
8. Failed Payments excluded from completed sales summaries
9. Refunded Orders summarized separately

---

## Calculated Columns Created

* cleaned_discount
* calculated_sales
* calculated_profit
* profit_margin
* shipping_delay_days
* order_month
* order_year
* data_quality_flag

---

## Data Quality Issues Identified

* Missing regions
* Missing ship modes
* Missing discounts
* Negative discounts
* Discount values stored as text percentages
* Date inconsistencies
* Invalid shipping records
* Status inconsistencies

---

## Pivot Reports Generated

### Report 1

Sales and Profit by Region

### Report 2

Sales and Profit by Category and Sub-Category

### Report 3

Order Count by Ship Mode

### Report 4

Profit Margin by Customer Segment

### Report 5

Refunded / Cancelled / Failed Orders by Region

### Report 6

Monthly Sales Trend

---

## Key Business Insights

* Certain regions contribute significantly more sales than others.
* Standard Class shipping is the most frequently used shipping method.
* Office Supplies and Technology categories generate substantial revenue.
* Several records contained invalid discount values.
* A small number of records contained shipping date issues.
* Refunded and cancelled orders impact overall profitability.

---

## Assumptions

* Maximum acceptable discount threshold = 50%.
* Missing discount values are treated as zero only when other financial values are valid.
* Unknown values are retained instead of deleted to preserve records.

---

## Limitations

* Analysis is limited to the provided dataset.
* Business logic assumptions were applied where requirements were not explicitly specified.
* Historical system-level validation was not available.

---

## Screenshots Included

* raw_data_preview.png
* cleaned_data_preview.png
* pivot_summary_1.png
* pivot_summary_2.png
