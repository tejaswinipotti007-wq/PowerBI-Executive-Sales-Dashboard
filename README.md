# Executive Sales & Performance Dashboard | Power BI Analytics

An executive-level Power BI solution designed to track top-line revenue, net profitability, regional growth, and product margins. Built using a formal Star Schema data model and dynamic DAX measures.

---

## 🧮 Core DAX Measures Created

| Measure Name | DAX Formula | Business Context |
| :--- | :--- | :--- |
| **Total Sales** | `Total Sales = SUM(Orders[sales])` | Aggregates gross sales volume. |
| **Total Profit** | `Total Profit = SUM(Orders[profit])` | Aggregates total net profit. |
| **Profit Margin** | `Profit Margin = DIVIDE([Total Profit], [Total Sales])` | Measures baseline operating margin percentage. |
| **Total Orders** | `Total Orders = COUNTROWS(Orders)` | Tracks total volume of order transactions. |
| **Previous Month Sales** | `Previous Month Sales = CALCULATE([Total Sales], PREVIOUSMONTH(Calendar[Date]))` | Calculates baseline prior-month sales for MoM tracking. |
| **Growth %** | `Growth % = DIVIDE([Total Sales] - [Previous Month Sales], [Previous Month Sales])` | Tracks MoM sales velocity % change. |
| **Category Contribution %** | `Category Contribution % = DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(products[category])))` | Evaluates relative category revenue share. |

---

## 💡 Strategic Business Insights

1. **Growth Consistency:** Monthly revenue exhibits MoM volatility, with cyclical peaks in Q3/Q4 driven by holiday spending and budget flushes.
2. **Top Revenue Region:** The **Central** region leads company-wide sales, followed by EMEA and South.
3. **Highest Margin Category:** **Technology** generates both highest sales volume and superior profit margins. **Furniture** yields lower relative profitability.
4. **Top Product Drivers:** **Phones** (~13.3%) and **Copiers** (~11.9%) represent the most valuable product lines.
5. **Key Management Recommendations:** 
   - Renegotiate supplier/freight contracts for the Furniture category.
   - Expand marketing investments in mid-tier sales regions.
   - Establish dedicated enterprise support for Top 10 high-value customers.

---

## 📁 Repository Deliverables
- `power_bi_task_4.pbix` - Interactive Power BI Report File
- `Executive_Business_Report.pdf` - Complete Written Executive Insight Report
-
