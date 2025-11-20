# Revenue Insights Project (Power BI)

This project is part of my data analytics work, where I created a Power BI dashboard to understand revenue patterns, customer behavior, and overall business performance. The main idea behind the project was to take raw sales data, clean and organize it, build a proper data model, and then create visuals that clearly explain what is happening in the business.

## 📊 Overview

The dashboard gives a clear picture of how the company is performing in terms of revenue, profit, and product categories. I tried to keep the design simple so that anyone can use the filters and explore the data without needing technical knowledge.

Some of the main things I focused on were:

* Total revenue and profit trends
* Which product categories perform better
* Customer segments and regional performance
* Month‑wise patterns and comparisons

## 📘 Project Overview

The dashboard follows a simple workflow:

1. **Data Import** – Loaded the dataset into Power BI.
2. **Cleaning & Transformation** – Removed duplicates, fixed data types, handled null values, and created new calculated columns.
3. **Data Modeling** – Created a star schema connecting fact and dimension tables.
4. **DAX Measures** – Wrote formulas to calculate revenue, profit, quantity, growth, etc.
5. **Dashboard Creation** – Used visuals like bar charts, line charts, maps, and tables.
6. **Insights** – Analyzed trends to understand business performance.


## 🧮 DAX Formulas Used

These are some of the DAX measures I used:

**Total Revenue**

```
Total Revenue = SUM(Sales[Revenue])
```

**Total Profit**

```
Total Profit = SUM(Sales[Profit])
```

**Profit Percentage**

```
Profit % = DIVIDE([Total Profit], [Total Revenue])
```

**Year‑over‑Year Growth**

```
YOY Revenue Growth = 
VAR CurrentYear = [Total Revenue]
VAR LastYear = CALCULATE([Total Revenue], DATEADD(Calendar[Date], -1, YEAR))
RETURN DIVIDE(CurrentYear - LastYear, LastYear)
```


## ⚙️ Power Query Steps

Some of the transformations I applied in Power Query included:

* Removing duplicate entries
* Replacing errors with default values
* Cleaning text fields
* Changing column types
* Splitting and merging fields when needed


## 📂 Dataset Description

The dataset mainly includes:

### **Sales Table**

* Order ID
* Product ID
* Customer ID
* Date
* Quantity
* Revenue
* Profit

### **Product Table**

* Product ID
* Category
* Sub‑Category

### **Customer Table**

* Customer ID
* Segment
* Region

### **Calendar Table**

* Date
* Month
* Year
* Quarter


## 🔍 Key Insights

Some of the observations I found from the dashboard:

* Revenue shows a steady increase over time.
* The Technology category contributes the most to revenue.
* Corporate customers generate higher sales compared to other segments.
* Some regions clearly outperform others.
* A few product segments show lower profitability and may need business attention.


## 📝 Brief Project Explanation

This project helped me understand how to work with real‑world data in a structured way. I learned how to:

* Clean data properly
* Build a data model that works
* Write DAX functions for KPIs
* Design dashboards that actually communicate insights
* Extract useful findings from the visuals

I also realized the importance of experimenting with different visuals before finalizing the dashboard.


