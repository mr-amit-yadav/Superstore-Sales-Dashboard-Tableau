# 🛒 Superstore Sales Tableau Dashboard
 
![Tableau](https://img.shields.io/badge/Tool-Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)
![Deployment](https://img.shields.io/badge/Deployed%20on-Tableau%20Public%20Cloud-E97627?style=flat-square&logo=tableau&logoColor=white)
![Status](https://img.shields.io/badge/Status-Live%20Project-brightgreen?style=flat-square)
![Dataset](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=flat-square&logo=kaggle&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)
 
An interactive, **live** Tableau dashboard analyzing Superstore sales performance across regions, time, and product pricing tiers - covering profit by region, order trends over time, sales distribution, and the profit-to-sales relationship. The dashboard is **deployed on Tableau Public Cloud** for public access.
 
🔗 **[View Live Dashboard on Tableau Public](https://public.tableau.com/app/profile/amit.yadav1803/viz/SuperstoreSalesTableauDashboard_17813572391830/Dashboard1)**
 
---
 
## 📊 Dashboard Preview
 
The dashboard combines 4 worksheet types into a single interactive view (`Dashboard 1`), each highlighting a different angle on sales and profitability.
 
| Worksheet | Type | Fields Used | Focus Area |
|---|---|---|---|
| `Bar Chart` | Bar | Region (rows), Sum of Profit (columns) | Profit by Region |
| `Line Chart` | Line | Order Date (columns, by month), Sum of Order Quantity (rows) | Order Quantity Trend Over Time |
| `Pie Chart` | Pie | Region (color/label), Sum of Sales (wedge size, % of total) | Sales Share by Region |
| `Scatter Plot` | Scatter | Sum of Sales (columns), Sum of Profit (rows) | Profit vs. Sales Relationship |
 
---
 
## 🧠 About the Dataset
 
- **Source:** [Kaggle](https://www.kaggle.com/) - Superstore Sales Dataset
- **Format:** Tableau Extract (.hyper), embedded in the packaged workbook for portability
- **Columns:** 22 total fields, spanning order details, customer info, product info, and shipping/financial metrics
### Key Fields Used
 
| Field | Description |
|---|---|
| Order ID / Row ID | Unique identifiers per record |
| Order Date / Ship Date | Date fields used for time-based trend analysis |
| Order Priority | Categorical urgency level of the order |
| Order Quantity | Number of units ordered |
| Sales / Profit / Discount | Core financial measures |
| Unit Price | Per-unit price, used as the basis for the calculated tier grouping |
| Shipping Cost / Ship Mode | Logistics-related fields |
| Customer Name / Customer Segment | Customer-level dimensions |
| City / State / Region / Zip Code | Geographic dimensions |
| Product Category / Sub-Category / Name / Container | Product-level dimensions |
| Product Base Margin | Underlying margin percentage per product |
 
---
 
## 🧮 Calculated Fields
 
| Field Name | Logic | Purpose |
|---|---|---|
| `Grouping Based On Unit Price` | `IF [Unit Price] <= 500 THEN 'B' ELSEIF [Unit Price] <= 2500 THEN 'A' ELSE 'C' END` | Buckets every order into a price tier - **B** (≤ ₹500), **A** (₹501–₹2500), or **C** (> ₹2500) - enabling tier-based filtering and analysis across all four worksheets |
 
---
 
## 🔍 Key Insights
 
- **Regional profit** varies noticeably across the four regions, with the Bar Chart surfacing which regions drive (or drag down) overall profitability.
- **Order Quantity trends** over time (Line Chart) reveal seasonal/monthly fluctuations in purchasing volume.
- **Sales share by Region** (Pie Chart) shows the proportional contribution of each region to total sales, with percentage labels for quick comparison.
- **Profit vs. Sales** (Scatter Plot) highlights the spread of orders - useful for spotting high-sales/low-profit outliers, a common red flag in discount-heavy orders.
- The **Unit Price tier grouping** allows slicing all four views by pricing segment (B / A / C), surfacing whether certain price bands are disproportionately driving profit or loss.
---
 
## 🗂️ Repository Structure
 
```
superstore-sales-tableau-dashboard/
│
├── README.md
└── Superstore Sales Tableau Dashboard.twbx     # Tableau packaged workbook (extract embedded)
```
 
---
 
## 🛠️ Tools Used
 
- **Tableau Desktop** - dashboard design & calculated fields
- **Tableau Public Cloud** - live deployment & public hosting
- **Kaggle** - source dataset
---
 
## 👤 Author
 
**Amit Yadav**
🔗 [LinkedIn](https://www.linkedin.com/) · [GitHub](https://github.com/mr-amit-yadav) · [Tableau Public Profile](https://public.tableau.com/app/profile/amit.yadav1803)
