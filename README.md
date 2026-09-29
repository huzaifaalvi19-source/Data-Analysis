# Data-Analysis
A collection of data analysis projects and practical exercises using Python, SQL, Power BI, and Excel. This repository demonstrates my work in data cleaning, exploratory analysis, visualization, querying, dashboard development, and extracting insights from data.
# **EXCEL**
<br>
# Excel Data Analysis Projects

Two end-to-end business analytics projects built entirely in Microsoft Excel: a **pizza sales dashboard** and a **customer segmentation model using RFM analysis**. Both cover data modeling, formula-driven calculations, pivot tables, and visual reporting.

## Repository Contents

| File | Project | Focus |
|------|---------|-------|
| `Dataset - Pizza Sales - Dashboard.xlsx` | Pizza Sales Dashboard | Sales performance, product mix, and ordering patterns |
| `Assignment # 2 RFM - Huzaifa.xlsx` | RFM Customer Segmentation | Customer value analysis and marketing strategy |

---

## 1. Pizza Sales Dashboard

An interactive Excel dashboard analyzing a full year of pizza orders (2015) to understand what sells, when, and at what value.

### Dataset
- **~48,600** order line items across **~21,350** orders
- **96** pizza SKUs (type, size, price, category, ingredients)
- Four source tables: `Orders`, `order_details`, `Pizzas`, and analysis sheets

### Approach
- Joined orders, order details, and the pizza catalog with **VLOOKUP** to build a single analysis-ready table
- Calculated **Sales** (`Price x Quantity`) and tagged each line as **Premium** or **Standard** using a sales threshold
- Summarized results with **pivot tables**, charts, and **slicers** for interactive filtering

### Business Questions Answered
1. What are the top-selling pizza categories by total quantity sold?
2. Which pizza sizes generate the highest revenue?
3. When is the peak time for pizza orders by total quantity?
4. Do certain categories sell better at particular times of day?
5. Do customers prefer Premium or Standard pizzas?
6. What is the average price of each pizza category?
7. How does total sales revenue change across months?

### Key Skills
Data modeling, lookup functions, calculated fields, pivot tables, slicers, dashboard design

---

## 2. RFM Customer Segmentation

A customer segmentation model that scores customers on **Recency, Frequency, and Monetary value** to identify who to reward, nurture, win back, or deprioritize.

### Dataset
- **~541,900** transaction rows of online retail data (Dec 2010 - Dec 2011)
- Fields: invoice, product, quantity, date, unit price, customer, country, and calculated revenue
- **4,372** unique customers segmented

### Approach
1. **Aggregate** transactions per customer with a pivot table: most recent purchase date, distinct invoice count (frequency), and total revenue (monetary value)
2. **Calculate recency** as days between each customer's last purchase and the dataset's maximum date
3. **Score each dimension from 1 to 5** using quintiles (`PERCENTILE.INC` at the 20th, 40th, 60th, and 80th percentiles)
4. **Combine** R, F, and M scores into an overall RFM score
5. **Assign segments** and visualize the distribution in a chart

### Segment Results

| Segment | Customers | Profile |
|---------|-----------|---------|
| Champions | 970 | Recent, frequent, high-spending; the best customers |
| Potential Loyalists | 349 | Recent with good spend, not yet frequent |
| New Customers | 279 | Very recent, but one-time or low spend |
| At-Risk Customers | 290 | Previously frequent, high-value, but gone quiet |
| Others / Need Attention | 2,484 | Below average across all three scores |

The workbook also includes a **Guide to RFM Segments** sheet that maps each segment to its score ranges and a recommended marketing strategy (loyalty perks for Champions, onboarding for New Customers, win-back campaigns for At-Risk, and so on).

### Key Skills
Customer analytics, percentile-based scoring, nested `IF` logic, `DATEDIF`, pivot tables, segmentation strategy

---

## Tools & Techniques

- **Microsoft Excel:** pivot tables, pivot charts, slicers, structured tables
- **Functions:** `VLOOKUP`, `IF`, `PERCENTILE.INC`, `DATEDIF`, `SUM`
- **Analytics:** sales analysis, time-based trends, product mix, RFM segmentation

## How to Use

1. Download the `.xlsx` files from this repository.
2. Open them in Microsoft Excel (2016 or later recommended; slicers and `PERCENTILE.INC` are used).
3. Explore the analysis sheets and dashboards; source data sits on the underlying sheets.

> Note: the RFM workbook is large (500K+ rows), so allow a moment for it to open.

## Author

**Muhammad Huzaifa**
Industrial Engineer | Data Analysis & Simulation
GitHub: [huzaifaalvi19-source](https://github.com/huzaifaalvi19-source)
