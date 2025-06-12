# 🏠 Airbnb Listings Analysis

*Paris market performance deep dive focusing on pricing dynamics and regulatory impact.*

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

Airbnb's growth in popularity has increased the focus on designing regulations to limit the number of properties listed in each city. 

### Goal: 

Leadership has asked to analyze Paris listings, with a focus on pricing, and to assess how the 2015 regulations impacted the Paris market.

### Tasks:

- Profile & QA the data: import the raw listings, cast date columns, filter for Paris, select key columns, and check for missing values & summary statistics.
- Prepare for visualization: create aggregated tables by neighborhood, accommodations, and host year.
- Visualize & derive insights: plot average prices by neighborhood and accommodates, chart new hosts & prices over time, and interpret the impact of regulations.
  
---

## 📂 Data

*All data was sourced from Maven Analytics*

**`paris_listings_sample.csv`**  
   - As the raw listings data was too big to upload on github, I've only uploaded the Paris sample. However the whole overview along with any step can be found on `AirBnB_Listings_Analysis_notebook.ipynb`

---

## 🚀 How to Open & Use

1. **Clone the repo**
 ```bash
git clone https://github.com/la-retrouvaille/Data-Analysis-Projects.git
cd Data-Analysis-Projects/AirBnB-Listing-Analysis
``` 

2. **Install dependencies**
```bash
pip install -r requirements.txt
``` 

3. **Launch Jupyter Notebook**
```bash
jupyter notebook
```

Open `AirBnB_Listings_Analysis_notebook.ipynb` and run all cells.

---

## 🔍 Key Findings

- **Élysée as most expensive neighbourhood**  

The Élysée district tops the list at €210.54, followed by Louvre (€175.38) and Passy (€161.14). This concentration in the city center reflects premium demand and limited supply in historic arrondissements.

![Average Listing Price by Paris Neighbourhood](screenshots/Average-Listing-Price-by-Neighbourhood.PNG) 

- **Friday & 10 AM Are Peak**
  
**Friday** has the highest transaction volume (*21,701*), while **Saturday** is the slowest (*20,510*).  
The busiest single hour is **10 AM** (*18,545 transactions*), likely by the breakfast rush.
    
- **Coffee Dominates, Tea a Close Second**
   
The **Coffee** category accounts for *58,416* item-level transactions, followed by **Tea** (*45,449*) and **Bakery** (*22,796*).
    
- **Top 3 Products by Volume**
  
  1. **Brewed Chai tea**: *17,183* transactions (*$77.1K*)  
  2. **Gourmet brewed coffee**: *16,912* transactions (*$70.0K*)  
  3. **Barista Espresso**: *16,403* transactions (*$91.4K*) - highest revenue per sale (~$5.58)
     
- **Locations Are Evenly Matched**  

Hell’s Kitchen leads slightly (*$236.5K*), with Astoria (*$232.2K*) and Lower Manhattan (*$230.1K*) very close behind.

---

### Recommendations

1. **Optimize Staffing & Hours**  
   - Staff more baristas between **8 AM-11 AM**, especially on **Fridays**, to handle peak loads.  
   - Consider light coverage or targeted promotions during the early afternoon slump (12-2 PM).

2. **Promote High-Margin Items**  
   - Upsell or bundle **Barista Espresso** (highest revenue per transaction) with bakery items.  
   - Feature **Gourmet brewed coffee** and **Chai tea** in loyalty rewards to drive repeat visits.

3. **Target Slow Periods**  
   - Launch a **“February Warm-Up”** promo (e.g., discount on hot chocolate) to mitigate winter lull.  
   - Use targeted email or app notifications when foot traffic is forecasted to dip.

---

## 📁 Folder Structure (Git Repo)

- **coffee-shop-sales/**
  - [Coffee Shop Sales.xlsx](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Coffee-Shop-Sales/Coffee%20Shop%20Sales.xlsx) <- Complete workbook (all three sheets)
  - [Coffee-Shop-Sales-Dashboard.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Coffee-Shop-Sales/Coffee-Shop-Sales-Dashboard.PNG) <- Screenshot of the dashboard
  - [.gitignore](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Coffee-Shop-Sales/.gitignore) <- Git rules: files/directories to ignore
  - [README.md](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Coffee-Shop-Sales/README.md) <- This file  

> *Note: The entire analysis lives in `Coffee Shop Sales.xlsx`. No extra folders or scripts are required.*

---

## 💻 Tech Stack & Dependencies

Microsoft Excel (PivotTables, PivotCharts, Slicers).

---

## 💡 Next Steps & Optional Enhancements
 
- **Add Weather Data**  

  Merge daily temperature/precipitation to analyze weather vs. sales correlations.

- **Compare Advanced Models**  

  Export `Transactions_processed` to CSV and build Python/R models for improved forecasting beyond Excel capabilities.

- **Interactive Web Dashboard**  

  Use Power BI to host a web-accessible version so stakeholders without Excel can explore filters live.

- **Automate Data Refresh**  

  Create a simple Python script to fetch new POS data daily and auto-refresh PivotTables.

- **Location-Specific Insights**

  Compare day-part performance by store to tailor local promotions.
  Analyze demographic or foot-traffic data around each café to inform menu or pricing strategies.    

---

## 👩‍💻 Licence & Credit

This project is licensed under the **MIT License** - see the [LICENSE](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LICENSE) file for details.

- **Data Source:** Fictional Maven Roasters POS Logs (Jan-Jun 2023) from Maven Analytics
- **Emojis & Icons:** [Emojipedia](https://emojipedia.org/)

---

## 📧 Contact

Egi Aliaj

[GitHub](https://github.com/la-retrouvaille) | [LinkedIn](https://www.linkedin.com/in/egialiaj/)

*Thank you for exploring this project! Feel free to ⭐ the repo if you found it helpful.*  
