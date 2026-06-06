# Excel Data Cleaning — Orders Dataset
### Week 1 | Decode Lab Internship

## Project Overview
This project involved identifying and resolving data quality
issues in a 1,200-row orders dataset using Microsoft Excel.
The goal was to produce a clean, analysis-ready dataset before
moving into exploratory data analysis in Week 2.

**Tool:** Microsoft Excel
**Dataset:** 1,200 rows · 14 columns · Jan 2023 – Jun 2025
**Internship:** Decode Lab | Training: TS Academy

---

## Dataset Structure

| Column | Data Type | Description |
|---|---|---|
| OrderID | Text | Unique order identifier |
| Date | Date | Order date |
| CustomerID | Text | Unique customer identifier |
| Product | Text | Product purchased |
| Quantity | Number | Units purchased |
| UnitPrice | Number | Price per unit |
| TotalPrice | Number | Total order value |
| OrderStatus | Text | Current order status |
| PaymentMethod | Text | Payment type used |
| CouponCode | Text | Discount code applied |
| ReferralSource | Text | Marketing channel |
| ItemsInCart | Number | Total items in cart |
| ShippingAddress | Text | Delivery address |

---

## Issues Found & Actions Taken

### 1. Date Column — Serial Numbers
- **Issue:** Date column stored as Excel serial numbers
instead of readable dates
- **Action:** Reformatted entire column to DD/MM/YYYY
date format
- **Rows affected:** All 1,200

### 2. Blank CouponCode Values
- **Issue:** 309 rows had no coupon code entry
- **Action:** Replaced all blank cells with "No Coupon"
using Find & Replace with Match Entire Cell Contents
- **Rows affected:** 309

### 3. TotalPrice Floating Point Errors
- **Issue:** 29 rows had floating point precision errors
e.g. 2357.7600000001 instead of 2357.76
- **Action:** Formatted column to 2 decimal places and
applied ROUND() formula to fix underlying values
- **Rows affected:** 29

### 4. Incomplete ShippingAddress
- **Issue:** All 1,200 addresses contained only a street
number with no city, state or zip code
- **Action:** Flagged for follow-up — data not fabricated
- **Rows affected:** All 1,200

### 5. Duplicate Check
- **Issue:** Checked for duplicate OrderIDs
- **Action:** Used Remove Duplicates — zero duplicates found
- **Rows affected:** None

### 6. TotalPrice Verification
- **Issue:** Needed to confirm TotalPrice accuracy
- **Action:** Verified TotalPrice = Quantity × UnitPrice
across all 1,200 rows — all values confirmed correct

---

## Key Cleaning Observations
- The dataset was in reasonable shape overall — no missing
values in critical columns and no duplicates
- The most significant issue was the 41.4% combined
cancellation and return rate discovered during verification
- CouponCode blanks (309 rows) were the largest missing
data issue but were intentional — customers with no coupon

---

## Tools & Techniques Used
- Excel Format Cells for date and number formatting
- Find & Replace for blank CouponCode values
- Conditional Formatting for duplicate highlighting
- ROUND() formula for floating point correction
- Remove Duplicates for duplicate detection
- Data Validation for column type enforcement

---

## Next Steps
Cleaned dataset used as input for:
- Week 2: Exploratory Data Analysis in Excel
- Week 3: SQL Analysis in SQL Server
- Week 4: Power BI Dashboard

---

## Author
**Adesola Jegede**
Data Analytics Intern — Decode Lab
Student — TS Academy
🔗 [LinkedIn]([https://www.linkedin.com/in/your-linkedin-url](https://www.linkedin.com/in/jegede-adesola-562398244))
