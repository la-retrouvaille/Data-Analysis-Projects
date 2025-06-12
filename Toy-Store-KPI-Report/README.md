# 🧸 Maven Toys KPI Dashboard 

*An interactive Power BI report to track key business metrics for a Mexican toy-store chain.*

---

## 📋 Table of Contents

1. [✨ Project Overview](#-project-overview)  
2. [📂 Data](#-data)  
3. [🚀 How to Open & Use](#-how-to-open--use)  
4. [🔍 Key Findings](#-key-findings)  
5. [📁 Folder Structure (Git Repo)](#-folder-structure-git-repo)
6. [💻 Tech Stack & Dependencies](#-tech-stack--dependencies)
7. [💡 Next Steps & Optional Enhancements](#-next-steps--optional-enhancements)  
8. [👩‍💻 Licence & Credit](#-licence--credit)
9. [📧 Contact](#-contact)

---

## ✨ Project Overview

### Situation:

Maven Toys is a growing toy-store chain operating multiple locations across Mexico. 

### Goal: 

Connect transactional and dimension data, define key measures, and deliver a Power BI report that shows current‐month KPIs and historical trends by store area and product category.

### Tasks:

- **Data profiling & QA**
  
  - Inspect `sales`, `products`, `stores`, and `calendar` tables  
  - Validate datatypes, nulls, primary/foreign keys  
  - Surface counts (transactions, stores) and price ranges
    
- **Relational model (star schema)**
  
  - Create tables & relationships   
  - Define a date-dimension with `date`, `start_of_week`, `start_of_month`  
  - Hide foreign-key columns in the reporting layer
    
- **Calculated measures**
  
  - Load `cost` & `price` into the fact table via JOINs  
  - Compute per-transaction **Revenue** and **Profit**  
  - Define DAX measures:  
    - `Total Orders`  
    - `Total Revenue`  
    - `Total Profit`
      
- **Interactive report**
  
  - KPI cards for current-month orders, revenue, and profit (with trend sparkline)  
  - Slicers for **Store Area** and **Product Category**  
  - Bar chart: **Orders** by **Product Category**  
  - Area/line chart: **Revenue** over time using the date hierarchy  
  
---

## 📂 Data

All source data is provided as CSV files. 

| Filename                        | Description                                       |
|---------------------------------|---------------------------------------------------|
|`calendar.csv`                   | Date dimension (date, day, month, year)           |
|`products.csv`                   | Product lookup (ID, category, price, cost)        |
|`sales.csv`                      | Transactional records, Jan 2022–Sep 2023          |
|`stores.csv`                     | Store lookup (ID, name, area, region, etc.)       |

---

## 🚀 How to Open & Use

1. **Clone the repo**
   
   ```bash
   git clone https://github.com/la-retrouvaille/data-analysis-projects.git
   cd data-analysis-projects/toy-store-kpi-report

2. **Open the Power BI report**

  - Launch Power BI Desktop
  - Open `Maven_Toys_KPI_Report.pbix`
  - Verify data source settings
  - Refresh the model and explore the dashboard

---

## 🔍 Key Findings

- **Current-Month KPIs**
  
  - Total Orders: 41 830
  - Total Revenue: $658 194
  - Total Profit: $180 445

- **Trend Insights**

  - Revenue dips in mid-2022, then peaks in early 2023 before settling.
  - Profit trends closely mirror revenue, with margin stability above 25%.

- **Category Performance**

  - Toys and Art & Crafts lead in order volume.
  - Electronics tracks lower but yields higher per-unit revenue.

![PowerBI Dashboard](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Toy-Store-KPI-Report/Maven_Toys_KPI_Report_Dashboard.PNG)

---

## 📁 Folder Structure (Git Repo)

**/Toy-Store-KPI-Report**

  - [Maven_Toys_KPI_Report.pbix](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Toy-Store-KPI-Report/Maven_Toys_KPI_Report.pbix) <- PowerBI Dashboard

  - [Maven_Toys_KPI_Report_Dashboard.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Toy-Store-KPI-Report/Maven_Toys_KPI_Report_Dashboard.PNG) <- A screenshot of the dashboard
 
  - [calendar.csv](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Toy-Store-KPI-Report/calendar.csv) <- source file

  - [products.csv](products.csv) <- source file

  - [sales.csv](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Toy-Store-KPI-Report/sales.csv) <- source file

  - [stores.csv](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Toy-Store-KPI-Report/stores.csv) <- source file
   
  - [.gitignore](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Toy-Store-KPI-Report/.gitignore) <- Git rules: files/directories to ignore

  - [README.md](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Toy-Store-KPI-Report/README.md) <- This file  

---

## 💻 Tech Stack & Dependencies

BI: Power BI Desktop

---

## 💡 Next Steps & Optional Enhancements
 
- **Enhanced visuals:** add geographic maps, drill‐through pages, custom themes

- **Advanced analytics:** integrate Python/R visuals for forecasting
  
---

## 👩‍💻 Licence & Credit

This project is licensed under the **MIT License** - see the [LICENSE](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LICENSE) file for details.

- **Data Source:** Maven Analytics
- **Emojis & Icons:** [Emojipedia](https://emojipedia.org/)

---

## 📧 Contact

Egi Aliaj

[GitHub](https://github.com/la-retrouvaille) | [LinkedIn](https://www.linkedin.com/in/egialiaj/)

*Thank you for exploring this project! Feel free to ⭐ the repo if you found it helpful.*  
