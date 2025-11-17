# BMW Worldwide Sales Analysis (2010–2024)

<img width="1132" height="641" alt="Executive Summary" src="https://github.com/user-attachments/assets/32e1cf16-dc0d-468d-a949-cca0d45ce6b8" />

## 📌 Overview
https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi
This project is a **Power BI dashboard** analyzing BMW worldwide sales from **2010 to 2024**. It provides insights into:
- Total Sales Volume
- Total Revenue
- Average Price
- Regional performance
- Model, Color, Fuel Type, and Engine Size trends

The dashboard is designed for **business decision-making**, enabling users to explore sales patterns and identify key drivers.

---

## ✅ Features
- **Multi-Page Dashboard**:
  - **Executive Summary**: KPIs, global trends, and regional performance.
  - **Performance by Model, Color & Fuel Type**: Category-level insights.
  - **Detailed Sales Analysis**: Drill-down with interactive filters including Engine Size.
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

<img width="1132" height="641" alt="Executive Summary" src="https://github.com/user-attachments/assets/d2afcf3a-9c53-446a-9b82-21431ec0312b" />


### 2. Performance by Model, Color & Fuel Type
- Bar Charts: Sales Volume, Revenue, and Average Price by Model
- Bar Charts: Sales Volume, Revenue, and Average Price by Color
- Bar Charts: Sales Volume, Revenue, and Average Price by Fuel Type

<img width="1135" height="645" alt="Performance by Model, Color   Fuel Type" src="https://github.com/user-attachments/assets/2f853568-a79a-4e47-ac06-50776b1bfb5c" />

### 3. Detailed Sales Analysis
- Interactive Table with filters:
  - Region, Year, Fuel Type, Transmission, Color, Engine Size
- Columns: **Model**, **Engine_Size_L**, **Price_USD**, **Net Sales**, **Sales_Volume**, **Mileage_KM**

<img width="1142" height="646" alt="Detailed Sales Analysis" src="https://github.com/user-attachments/assets/b1a16493-f953-416a-b7b1-630d76af3d33" />


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


