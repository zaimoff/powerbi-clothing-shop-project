# 📊 Sales Performance Dashboard — Power BI Project

A comprehensive, interactive sales analytics dashboard built in Power BI, analysing sales performance across products, locations, customers, and time. The report enables stakeholders to explore revenue, profitability, and customer behaviour through a rich set of visuals and dynamic filters.

---

## 📁 File

| File | Description |
|------|-------------|
| `VasilZaimov_Project.pbix` | Main Power BI Desktop report file |

---

## 🗂️ Data Model

The project follows a **Star Schema** architecture with one central fact table and four dimension tables, plus a dedicated measures table.

```
DimDate ──────┐
DimProduct ───┤
              ├──► FactSales ◄── MyMeasures (calculated measures)
DimCustomer ──┤
DimLocation ──┘
```

### Tables

| Table | Type | Key Columns |
|-------|------|-------------|
| `FactSales` | Fact | Sales amount, Quantity, Unit Price, Cost |
| `DimDate` | Dimension | Date, Year, QuarterName, QuarterYear, MonthName |
| `DimProduct` | Dimension | Category, Brand, Color |
| `DimCustomer` | Dimension | Gender, CustomerAgeBucket |
| `DimLocation` | Dimension | State, City |
| `MyMeasures` | Measures table | 7 DAX measures |

---

## 📐 DAX Measures

All measures are organised in a dedicated `MyMeasures` table:

| Measure | Description |
|---------|-------------|
| `Total Sales` | Sum of all sales revenue |
| `Total Quantity` | Sum of units sold |
| `Average Unit Price` | Average price per unit |
| `Total Cost` | Sum of total cost |
| `Total Profit` | Total Sales minus Total Cost |
| `Repeat Customers Count` | Count of customers with more than one purchase |
| `Customer Count New vs Old` | Segmentation of new vs returning customers |

---

## 📊 Report Visuals

The dashboard is a single scrollable page (1280 × 3000 px) with 23 visuals organised into logical sections:

### KPI Cards
- Total Sales
- Total Quantity
- Average Unit Price
- Total Cost
- Total Profit

### Filters / Slicers
- Year (list)
- Quarter (list)
- Month (list)
- Date Range (between — from 2022-01-01)

### Charts & Tables

| Visual | Type | What It Shows |
|--------|------|---------------|
| Sales Over Time | Line Chart | Monthly sales trend, broken down by year |
| Sales by Product Category | Bar Chart | Revenue per product category |
| Sales by Brand | Column Chart | Revenue per brand |
| Sales by State | Column Chart | Revenue by geographic state |
| Sales by City | Bar Chart | Revenue by city |
| Quantity by Brand & Color | Matrix | Cross-tab of quantity sold by brand and colour |
| Quantity by Category & Brand | Matrix | Cross-tab of quantity sold by category and brand |
| Sales by Customer Age Group | Pie Chart | Revenue share across age buckets |
| Sales by Gender | Donut Chart | Revenue split by customer gender |
| Sales & Profit by Quarter | Clustered Column | Side-by-side quarterly comparison |
| Sales & Profit by Month | Bar Chart | Monthly profitability trend |
| Price vs Sales vs Profit | Scatter Chart | Three-variable analysis by product category |
| Customer Retention Trend | Stacked Area Chart | New vs repeat customers over time by quarter |

---

## ⚙️ Technical Details

| Property | Value |
|----------|-------|
| Power BI Desktop Version | 2025.08 (v2.146.304.0) |
| Created From | Power BI Cloud |
| Report Pages | 1 |
| Canvas Size | 1280 × 3000 px |
| Theme | CY24SU10 (built-in) |
| DataModel Compression | XPress9 / VertiPaq |
| Relationships | Manually defined (auto-detect disabled) |
| Cross-visual Filtering | Enabled |
| Enhanced Tooltips | Enabled |

---

## 🚀 Getting Started

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Clone or download this repository
3. Open `VasilZaimov_Project.pbix` in Power BI Desktop
4. Connect or refresh the data source as needed

---

## 👤 Author

**Vasil Zaimov**  
[LinkedIn](#) · [GitHub](#)
