📊 Retail Sales Analytics Dashboard (Power BI)

An interactive Power BI dashboard that analyzes retail sales data to uncover revenue trends, top-performing products, and regional performance, helping business teams make faster, data-driven decisions.

![Dashboard Preview](images/dashboard_preview.png)

---

## 🎯 Objective

To clean raw retail sales data, model it, and build a single-page dashboard that answers key business questions:

- How are sales and profit trending over time?
- Which products and categories drive the most revenue?
- Which regions or stores perform best and worst?
- What are the key KPIs a manager should track?

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI** | Data modeling, visualization, dashboard design |
| **DAX** | Measures, KPIs, calendar table, time intelligence |
| **Excel / CSV** | Source data and cleaning |
| **Python (Pandas)** | Data cleaning and preparation *(edit if applicable)* |

---

## 📁 Repository Structure

```
Retail-Sales-Analytics/
│
├── data/
│   └── retail_sales_cleaned.csv        # Cleaned dataset
│
├── dax/
│   └── DAX_Measures_and_Calendar.txt   # All DAX measures + calendar table
│
├── theme/
│   └── Retail_Sales_Theme.json         # Custom Power BI theme
│
├── docs/
│   ├── PowerBI_Build_Guide.txt         # Step-by-step build guide
│   └── Dashboard_Preview.pdf           # PDF preview of the report
│
├── images/
│   └── dashboard_preview.png           # Dashboard screenshot
│
├── Retail_Sales_Analytics.pbix         # Power BI file
└── README.md
```

---

## 🧹 Data Preparation

1. Removed duplicates and handled missing values
2. Standardized column names and data types
3. Fixed inconsistent date formats
4. Created a dedicated **Calendar table** for time intelligence
5. Exported the final dataset as `retail_sales_cleaned.csv`

---

## 📐 Key DAX Measures

```DAX
Total Sales = SUM(retail_sales_cleaned[Sales])

Total Profit = SUM(retail_sales_cleaned[Profit])

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Calendar'[Date]))

YoY Growth % = DIVIDE([Total Sales] - [Sales LY], [Sales LY], 0)
```

> Replace with your actual column names. Full list is in `dax/DAX_Measures_and_Calendar.txt`.

---

## 📈 Dashboard Features

- **KPI cards:** Total Sales, Total Profit, Profit Margin %, Orders
- **Trend analysis:** Monthly and yearly sales trend
- **Category and product analysis:** Top 10 products, sales by category
- **Regional analysis:** Sales and profit by region/store
- **Interactive slicers:** Year, month, category, region
- **Custom theme** for a clean, consistent look

---

## 💡 Key Insights

*(Replace with your real findings)*

- Sales peaked in **[month/quarter]**, driven by **[category]**
- **[Category/Product]** contributed the highest revenue, about **[X]%** of total sales
- **[Region]** had the highest profit margin, while **[Region]** underperformed
- Recommendation: **[one actionable suggestion]**

---

## 🚀 How to Use

1. Clone this repository
   ```bash
   git clone https://github.com/<your-username>/Retail-Sales-Analytics.git
   ```
2. Open `Retail_Sales_Analytics.pbix` in **Power BI Desktop**
3. If the data source path breaks, go to **Transform Data → Data source settings** and point it to `data/retail_sales_cleaned.csv`
4. (Optional) Import the theme: **View → Themes → Browse for themes → `Retail_Sales_Theme.json`**

---

## 📚 What I Learned

- Building a star-schema style data model in Power BI
- Writing DAX for KPIs and time intelligence
- Designing dashboards that are clear for non-technical users
- Turning raw data into business insights

---

## 👤 Author

**Sundhar V**
MBA (Business Analytics) | Aspiring Data Analyst

📍 Puducherry, India
🔗 [LinkedIn](https://www.linkedin.com/in/your-profile)
📧 your-email@example.com

⭐ If you found this project useful, feel free to star the repo!

