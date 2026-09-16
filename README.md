

# E-commerce Customer Behavior Analysis

Analysis of customer purchasing behavior in an e-commerce platform — pattern detection, segmentation, and satisfaction prediction.

This project analyzes 350 customers from an e-commerce platform, with 11 variables (age, city, membership type, spending, rating, and more). We used SQL for analysis, Excel for documentation and visualization, and Power BI for an interactive dashboard.

---

##  Research Questions

1. What is the distribution of customers by Membership, and what is the average spend per category?
2. What distinguishes "Satisfied" customers from "Neutral" and "Unsatisfied"?
3. Customers who repurchased early vs. late — what is the difference between them?
4. What is the ideal customer profile?

---

##  Dataset

- **Source:** Kaggle — E-commerce Customer Behavior Dataset
- **Size:** 350 rows, 11 columns
- **Main columns:** Customer ID, Gender, Age, City, Membership Type, Total Spend, Items Purchased, Average Rating, Discount Applied, Days Since Last Purchase, Satisfaction Level

---
##  Tools

| Tool | Usage |
|------|-------|
| **MySQL** | Data loading, 4 analytical queries |
| **Excel** | 6 sheets — Data + 4 questions + summary |
| **Power BI** | Interactive dashboard with 6 visuals |

---

##  Project Structure

```
ecommerce-customer-analysis/
├── README.md
├── sql/
│ └── ecommerce_db.sql
├── excel/
│ └── ecommerce_analysis.xlsx
├── powerbi/
│ └── ecommerce_dashboard.pbix
└── docs/
└── project_notes.docx
```

---

##  How to Run

**1.** Load data into MySQL:
```sql
CREATE DATABASE ecommerce_db;
USE ecommerce_db;
-- Import CSV file into the customers table
```

**2.** Run the queries:
```sql
SELECT membership_type,
       COUNT(customer_id) AS num_customers,
       ROUND(AVG(total_spend), 2) AS avg_spend
FROM customers
GROUP BY membership_type;
```

**3.** Open the Power BI report:
- Open `ecommerce_dashboard.pbix`
- The report will load automatically

 ## Key Results
 
| # | Question | Result |
|---|----------|--------|
| 1 | Distribution by Membership | Gold: $1,311 / Silver: $748 / Bronze: $473 |
| 2 | Satisfied customers | $1,280 spend, returned within 17 days |
| 3 | Repurchase patterns | Fast: $1,264 / Slow: $598 |
| 4 | Ideal customer | 73 Gold customers, age 29, spend $1,404 |

 ## Insights
 
- Gold members spend 2.8× more than Bronze members
- Satisfied customers returned within 17 days on average — compared to 43 days for unsatisfied customers
- Not repurchasing does not necessarily indicate dissatisfaction
- Every ideal customer is a Gold member — but not every Gold member is an ideal customer

 License
CC0-1.0 — Compatible with the original Kaggle dataset license.

 Contact
Name: Elene Salomon

GitHub: [https://github.com/fakemailforme14-cloud]
