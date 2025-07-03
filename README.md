# Amazon Product Data Analysis Using Microsoft Excel

This project presents a comprehensive analysis of Amazon product listings with a focus on **pricing**, **discounts**, **ratings**, and **customer engagement**. Using **Microsoft Excel**, the dataset was cleaned, transformed, and visualized through **PivotTables**, **formulas**, and **charts** to extract meaningful business insights.

---

## Objectives

1. Clean and prepare the dataset for analysis.
2. Use PivotTables, formulas, and charts to uncover actionable insights.
3. Visualize key relationships such as **rating vs. discount**.
4. Answer **14 business-driven questions** to support decision-making.

---

## Data Cleaning

Performed in Excel before analysis:

- Removed symbols like ₹ and % from numeric fields.
- Converted `actual_price`, `discounted_price`, `rating`, and `rating_count` to numeric types.
- Extracted `main_category` from multi-level category fields.
- Created a `price_bucket` column based on `actual_price`:
  - `<₹200`, `₹200–₹500`, `>₹500`
- Created `potential_revenue` = `actual_price × rating_count`
- Structured data into an Excel Table (Ctrl + T) for dynamic PivotTables.

---

## Key Business Questions & Methods

| # | Business Question | Excel Method |
|--:|-------------------|--------------|
| 1 | Avg. discount % by category | PivotTable (Average `discount_percentage` by `main_category`) |
| 2 | Product count per category | PivotTable (Count of `product_id` by `main_category`) |
| 3 | Total reviews per category | PivotTable (Sum of `rating_count` by `main_category`) |
| 4 | Top-rated products | PivotTable (Avg `rating` by `product_name`, sorted) |
| 5 | Avg actual vs discounted price | PivotTable (Avg `actual_price` & `discounted_price` by category) |
| 6 | Most reviewed products | PivotTable (Sum of `rating_count` by `product_name`, sorted) |
| 7 | Products with ≥50% discount | Helper column + PivotTable (Filter on `discount_percentage`) |
| 8 | Rating distribution | Rounded `rating` column + PivotTable |
| 9 | Potential revenue by category | PivotTable (Sum of `potential_revenue` by `main_category`) |
| 10 | Product count by price range | PivotTable (`price_bucket` vs. product count) |
| 11 | Rating vs Discount | Scatter plot (`rating` vs `discount_percentage`) |
| 12 | Products with <1000 reviews | `COUNTIF` or filter (`rating_count` < 1000) |
| 13 | Highest avg. discounts by category | PivotTable (Avg `discount_percentage`, sorted) |
| 14 | Top 5 hybrid-score products | Formula: `rating × LOG10(rating_count + 1)` |

---

## Tools Used

- Microsoft Excel 2016+
- Excel Tables (Ctrl + T)
- PivotTables
- Formulas: `IF`, `LEFT`, `FIND`, `ROUND`, `LOG10`, `COUNTIF`
- Charts: Scatter plot, column chart, bar chart
-  Conditional Formatting & Filters

---

## Visualizations

- Category-wise discount & product counts
- Rating distribution histogram
- Rating vs Discount scatter plot
- Revenue and review contribution by category

---

## Key Insights

- Clean data is essential for reliable analytics.
- PivotTables allow fast multi-dimensional exploration.
- Visuals enhance the understanding of hidden trends (e.g., high-rated discounted products).
- Hybrid formulas help rank products more meaningfully.

---

## Author

**Student:** *[Richard IKhazobor Ayemhere]*  
**Institution:** *[Digital Slillup Africa]*  
**Course:** *Data Analytics *

