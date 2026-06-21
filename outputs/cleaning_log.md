# Cleaning Log

## Issues Found

### Text Issues

* Mixed capitalization
* Extra spaces
* Inconsistent category names
* Inconsistent shipping mode names

### Missing Data Issues

* Missing region values
* Missing ship mode values
* Missing discount values

### Discount Issues

* Negative discounts
* Excessive discounts
* Percentage values stored as text

### Date Issues

* Missing dates
* Invalid dates
* Ship date before order date

### Status Issues

* Cancelled orders
* Refunded orders
* Failed payments

---

## Cleaning Actions Performed

### Text Cleaning

Applied:

* TRIM
* Find and Replace
* Standardized capitalization
* Category normalization

### Missing Values

Region:

* Filled with Unknown

Ship Mode:

* Filled with Unknown

Discount:

* Filled with 0 where valid

### Date Validation

Validated:

* Missing dates
* Invalid dates
* Shipping sequence issues

### Discount Validation

Flagged:

* Negative discounts
* Discounts above allowed threshold

### Quality Flags

Assigned:

* CLEAN
* WARNING
* INVALID

---

## Business Rules Applied

1. Missing Region → Unknown
2. Missing Ship Mode → Unknown
3. Missing Discount → 0
4. Negative Discount → Invalid
5. Excessive Discount → Invalid
6. Ship Date before Order Date → Invalid
7. Cancelled Orders excluded from completed sales
8. Failed Payments excluded from completed sales
9. Refunded Orders reported separately

---

## Duplicate Handling

Checked for:

* Exact duplicate rows
* Duplicate Order IDs
* Conflicting duplicate records

Conflicting records were flagged for review instead of automatic deletion.

---

## Records Removed

Only confirmed exact duplicates were eligible for removal.

No conflicting business records were deleted automatically.

---

## Records Flagged

Flagged categories:

* Invalid discounts
* Shipping issues
* Missing critical values
* Calculation mismatches

---

## Limitations

* Source system validation unavailable.
* Business assumptions used where documentation was unavailable.
* Data quality findings depend on provided dataset only.
