
# 📊 Global Superstore Analysis – Documentation

## 📌 Project Overview
This project is a Power BI dashboard analyzing sales performance, profit, return rates, and regional trends using Excel as a data source, Power Query for data transformation, and DAX for advanced analytics.

---

## 🧹 Data Cleaning (Power Query - Excel & Power BI)

- Converted Order Date and Ship Date to proper Date format
- Changed Sales, Profit, and Shipping Cost to Decimal type
- Standardized text fields (Segment, Ship Mode, Category)
- Handled missing values in Postal Code column
- Ensured consistency across all datasets before modeling

---

## 🔗 Data Modeling

- Established relationship between Orders and People using Region
- Connected Orders and Returns tables using Order ID
- Built a relational model to support analysis in Power BI

---

## 📐 DAX Measures

### 1. Net Total Profit
Net Total Profit = SUM(Orders[Profit])

### 2. Net Sales
Net Sales = SUMX(Orders, Orders[Sales] * (1 - Orders[Discount]))

### 3. Average Shipping Cost
Avg Shipping Cost = AVERAGE(Orders[Shipping Cost])

### 4. Return Rate %
Return Rate % = DIVIDE(COUNTROWS(Returns), COUNTROWS(Orders))

---

## 📊 Key Analysis Areas

- Sales performance by Category
- Profit distribution by Region
- Manager performance evaluation
- Return rate impact on profitability
- Contribution analysis across business segments

---

## 📌 Tools Used

- Microsoft Excel (Data Source)
- Power BI (Visualization & Dashboard)
- Power Query (Data Cleaning)
- DAX (Calculated Measures)

---

## 💡 Key Insight

The business shows strong revenue performance, but profitability is impacted by a high return rate (22%). Technology is the primary revenue driver, indicating a dependency that may pose concentration risk. Additionally, profit distribution across managers is uneven, with performance concentrated among a few individuals.
