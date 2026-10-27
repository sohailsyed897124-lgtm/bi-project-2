# 🍽️ Zomato Sales Dashboard (Power BI)

An interactive Power BI dashboard that turns 6,000 Zomato food-delivery orders into clear business insights: revenue, orders, top cities, cuisines, restaurants, payment modes and peak ordering hours.

![Zomato Sales Dashboard](images/dashboard.png)

## 📌 Project Overview
Food-delivery platforms generate huge amounts of order data. This project cleans that data, builds key measures in DAX, and presents the results in a single interactive dashboard where clicking any chart filters all the others.

## 🎯 Objectives
- Clean and prepare food-order data for analysis
- Calculate revenue, total orders and average order value
- Identify the best-performing cities, cuisines and restaurants
- Find peak ordering hours
- Build an interactive dashboard with cross-filtering

## 🛠️ Tools Used
- Microsoft Power BI Desktop
- DAX (measures)
- CSV dataset

## 📂 Dataset
- **Records:** 6,000 orders (1 Jan 2025 – 30 Sep 2026)
- **Cities:** Hyderabad, Bengaluru, Mumbai, Delhi, Chennai, Pune, Kolkata
- **Columns:** Order_ID, Order_Date, Order_Hour, City, Restaurant_Name, Cuisine, Food_Type, Customer_Type, Order_Value, Discount_Amount, Delivery_Fee, Final_Amount, Payment_Mode, Delivery_Time_Min, Customer_Rating, Order_Status

> **Note:** This is a realistic sample dataset created for the project, not Zomato's confidential internal data. Restaurant names are illustrative.

## 🧹 Data Cleaning
- Removed duplicate orders
- Set correct data types (dates, numbers, text)
- Kept blanks only where logical (cancelled orders have no delivery time or rating)
- Standardised city, cuisine and status spellings
- Created date fields: Year, Month Name, Month No, Day Name

## 📐 DAX Measures
| Measure | Description |
|---|---|
| Total Revenue | Sum of Final_Amount for **delivered** orders only |
| Total Orders | Count of all orders |
| Avg Order Value | Revenue ÷ number of delivered orders |
| Avg Delivery Time | Average delivery minutes |
| Avg Rating | Average customer rating |
| Total Discount | Sum of discounts given |

## 📊 Dashboard Contents
- **KPI cards:** Total Revenue, Total Orders, Avg Order Value
- **Charts:** Revenue by month (2025 vs 2026), Orders by payment mode, Revenue by restaurant, Orders by cuisine, Revenue by city, Orders by hour
- **Slicers:** City, Cuisine, Customer Type, Order Date

## 🔍 Key Findings
| Measure | Result |
|---|---|
| Total orders | 6,000 |
| Total revenue | ~₹16.9 lakh |
| Avg order value | ~₹302 |
| Avg delivery time | ~34 minutes |
| Avg rating | ~4.1 / 5 |
| Total discounts | ~₹1.78 lakh |

- **Top city:** Bengaluru (~₹3.73 lakh), followed by Hyderabad, Mumbai and Delhi
- **Top cuisine:** Biryani (1,321 orders, ~₹4.52 lakh)
- **Top restaurants:** Meghana Foods, Paradise Biryani, Behrouz Biryani
- **Peak hours:** 8 PM and 7 PM (dinner), 12 PM (lunch)
- **Busiest days:** Saturday and Sunday
- **Payments:** UPI ~50%, Card ~26%, Cash on Delivery ~14%, Wallet ~10%
- **Customers:** ~50% returning, ~25% new, ~25% Gold members

## 💡 Business Recommendations
- Add more delivery partners at lunch and dinner peaks
- Run weekend offers
- Promote biryani restaurants
- Grow Pune and Kolkata with city-specific offers
- Encourage UPI payments

## ⚠️ Limitations
- Sample data of 6,000 orders, not the full Zomato dataset
- 2026 covers only nine months
- No area-level location or item-level detail

## 🚀 Future Scope
- Use larger, real datasets with live connections
- Add forecasting
- Add map visuals
- Publish to Power BI Service

## 📁 Repository Structure
```
zomato-sales-dashboard/
├── README.md
├── dashboard/     → Zomato_Sales_Dashboard.pbix
├── data/          → zomato_orders.csv
├── images/        → dashboard.png
└── docs/          → Zomato_Sales_Dashboard_Project_Report.pdf
```

## ▶️ How to Open
1. Download or clone this repository
2. Open the `.pbix` file in **Power BI Desktop**
3. If asked, update the data source path to the CSV in the `data/` folder

## 👤 Author
**Syed Sohail**
