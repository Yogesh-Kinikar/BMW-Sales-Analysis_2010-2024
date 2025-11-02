# BMW Worldwide Sales Analysis (2010–2024)

<img width="1147" height="645" alt="image" src="https://github.com/user-attachments/assets/3665c884-474c-4984-98a2-4bf4b9186992" />

## 📌 Overview
This project is a **Power BI dashboard** analyzing BMW worldwide sales from **2010 to 2024**. It provides insights into:
- Total Sales Volume
- Total Revenue
- Average Price
- Regional performance
- Model, Color, and Fuel Type trends

The dashboard is designed for **business decision-making**, enabling users to explore sales patterns and identify key drivers.

---

## ✅ Features
- **Multi-Page Dashboard**:
  - **Executive Summary**: KPIs, global trends, and regional performance.
  - **Performance by Model, Color & Fuel Type**: Category-level insights.
  - **Detailed Sales Analysis**: Drill-down with interactive filters.
- **Interactive Filters**: Year, Region, Fuel Type, Transmission, Color, Engine Size.
- **Visuals**: Line charts, bar charts, maps, scatter plots, and tables.
- **KPIs**: Total Sales Volume, Total Revenue, Average Price.

---

## ✅ Pages & Visuals
### 1. Executive Summary
- KPIs: Total Sales Volume, Total Revenue, Average Price
- Line Chart: Net Sales by Year
- Map: Net Sales by Region
- Bar Chart: Sales Volume by Region

![Executive Summary](screenshots/executive_summaryolor & Fuel Type
- Bar Charts: Sales Volume, Revenue, and Average Price by Model
- Bar Charts: Sales Volume, Revenue, and Average Price by Color
- Bar Charts: Sales Volume, Revenue, and Average Price by Fuel Type

![ategory Performance

### 3. Detailed Sales Analysis
- Interactive Table with filters:
  - Region, Year, Fuel Type, Transmission, Color, Engine Size
- Columns: Model, Price, Net Sales, Sales Volume, Mileage

![etailed Analysis

---

## ✅ Dataset Description
| Column              | Description                              |
|---------------------|------------------------------------------|
| Model              | BMW car model (e.g., 3 Series, X5)      |
| Year               | Year of sale (2010–2024)                |
| Region             | Geographic region                       |
| Fuel_Type          | Petrol, Diesel, Hybrid                 |
| Transmission       | Manual or Automatic                    |
| Engine_Size_L      | Engine size in liters                  |
| Mileage_KM         | Mileage in kilometers                  |
| Price_USD          | Price in USD                           |
| Sales_Volume       | Number of units sold                   |
| Net Sales          | Total revenue for that model           |

---

## ✅ DAX Measures Used
```DAX
Total Sales Volume = SUM('BMW'[Sales_Volume])
Total Revenue = SUM('BMW'[Price_USD])
Average Price = AVERAGE('BMW'[Price_USD])
Net Sales By Region = CALCULATE(SUM('BMW Project'[Net Sales]), ALLEXCEPT('BMW Project','BMW Project'[Region]))
