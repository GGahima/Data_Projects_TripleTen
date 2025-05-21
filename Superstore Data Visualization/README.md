readme_content = """
# Superstore Profitability Analysis

## 📘 Project Description

This project provides a comprehensive analysis of Superstore's operations with the objective of increasing profitability and avoiding potential bankruptcy. Using transactional and return data, we investigate product and regional performance, return rates, and advertising opportunities. Tableau was used to produce visual insights, and recommendations were made to support strategic decision-making.

---

## 📊 Analysis and Results

### Part 1: Product and Subcategory Analysis

#### ✅ Top 2 Profit Centers:
- **Chairs**
- **Phones**

#### ❌ 2 Biggest Loss-Makers:
- **Tables**
- **Bookcases**

#### 🔎 Discontinued Product Recommendation:
Using a scatterplot of *Profit vs. Sales by Product Name*, products with:
- High sales but negative profit were flagged for discontinuation.
- Visualizations clearly indicated several **Table** and **Bookcase** SKUs in this category.

#### 📌 Subcategory Recommendations:
**Focus On (High Margin & Volume):**
- Phones
- Binders
- Chairs

**Discontinue (Low/Negative Profit):**
- Tables
- Bookcases
- Supplies

> **Visualization Used:** Bubble chart with axes representing total sales and total profit per subcategory; size indicating order count.

---

### Part 2: Advertising Strategy by Region and Time

#### 📈 Top 3 State-Month Advertising Opportunities:
1. **California – November**
2. **New York – December**
3. **Texas – October**

#### 📊 Visualization:
A line chart displaying *Average Monthly Profit by State* shows profit spikes in these three combinations.

#### 📣 Advertising Investment Strategy:
We recommend investing proportionally to the profit potential:
- **California (Nov):** $15,000
- **New York (Dec):** $12,000
- **Texas (Oct):** $10,000

Budget allocation considers both the historical profit peak and return on marketing investments in similar months.

---

### Part 3: Returns and Risk Analysis

#### ✅ Calculated Field for "Returned":
```sql
IF ISNULL([Returned]) THEN 0
ELSEIF [Returned] = "Yes" THEN 1
END
