# 📊 Sales Performance Dashboard

Enterprise-level Tableau dashboard with YoY analysis, KPIs, and actionable business insights.


<img width="1600" height="1000" alt="WhatsApp Image 2026-04-18 at 09 38 09" src="https://github.com/user-attachments/assets/d86e0d9a-98a4-4135-bf6b-1151e8637ca9" />



**🔗 [View Live on Tableau Public](#)** *(Publishing soon)*

---

## Overview

Interactive sales analytics dashboard built following Mercedes-Benz enterprise standards. Analyzes 9,994 orders across 793 customers, 1,862 products, and 4 regions.

**Key Features:**
- 🎚️ Dynamic year selection via parameters
- 📊 KPI tracking with sparklines (Sales, Profit, Quantity)
- 📈 Bar-in-bar subcategory comparison
- 📉 Weekly trends with above/below average indicators
- 🎛️ Interactive filtering by product and location

---

## Key Insights

### Performance Highlights
- **Total Sales:** $2.3M across 9,994 orders
- **YoY Growth:** 20.4% (2022-2023)
- **Profit Margin:** 11.6% overall
- **Top Category:** Technology ($836K, 36% of sales, 14.2% margin)

### Top Performers
1. **Phones** - $330K (14.3% of total)
2. **Chairs** - $328K (14.2% of total)
3. **Storage** - $224K (9.7% of total)

### Problem Areas ⚠️
- **Tables:** -$17.7K profit (negative margin)
- **South Region:** Only 17% of sales (opportunity)
- **Discount Impact:** Heavy discounting reducing margins

---

## Recommendations

### Immediate Actions
1. **Fix Negative Margins**
   - Tables: 15-20% price increase → convert -$17.7K to +$23K
   - Machines: Cap discounts, bundle with accessories

2. **Optimize Discounts**
   - Cap at 15% for furniture
   - Reserve 20%+ for Technology only
   - Expected impact: +2-3% margin improvement

3. **Expand South Region**
   - Currently 17% vs 31% in West
   - Potential: +$150-200K annual revenue

### Expected Impact
- **Revenue:** +15-18% ($345-414K)
- **Profit:** +25-30% ($67-82K)
- **Margin:** 11.6% → 14-15%

---

## Technical Implementation

**Data Model:** Star schema
- Orders (Fact): 9,994 rows
- Customers: 793 unique
- Products: 1,862 items (3 categories, 17 subcategories)
- Locations: 531 postal codes (4 regions)

**Key Calculations:**

```tableau
Current Year Sales:
IF YEAR([Order Date]) = [Select Year Parameter]
THEN [Sales] ELSE NULL END

YoY % Change:
(SUM([Current Year]) - SUM([Previous Year])) / SUM([Previous Year])

Above/Below Average (Table Calc):
IF SUM([Sales]) > WINDOW_AVG(SUM([Sales]))
THEN "Above" ELSE "Below" END
```

**Technologies:**
- Tableau calculated fields & LOD expressions
- Parameters for dynamic year selection
- Table calculations (WINDOW functions)
- Dual-axis charts for comparisons
- Container architecture with 10px/7px spacing

---

## Getting Started

1. Download `Sales_Dashboard.twb` and CSV files
2. Open in Tableau Desktop/Public (2023.1+)
3. Select year from parameter dropdown
4. Click charts to cross-filter
5. Hover for detailed tooltips

---

## Skills Demonstrated

✅ Data modeling (star schema design)  
✅ Business analytics (identified $17.7K loss in Tables)  
✅ Advanced Tableau (LOD, WINDOW calculations, parameters)  
✅ Dashboard UX (4-color palette, professional formatting)  
✅ Strategic thinking (actionable recommendations with ROI)  


---

## Contact

**Ayham Bokli Hasan**  
Data Analyst | Tableau | SQL | Python  
📍 Berlin, Germany  
📧 ayham.bokli.hasan@gmail.com  
💼 [LinkedIn](https://linkedin.com/in/ayham-bokli)

---

⭐ **If this helped you, please star the repo!**
