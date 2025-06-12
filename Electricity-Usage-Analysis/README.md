# ⚡ Electricity Usage Analysis

*Assessing hourly and weekday demand patterns to inform infrastructure upgrades for Morocco's National Power Co.*

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

Morocco's National Power Co. is planning to upgrade its grid infrastructure to better handle peak loads and prevent outages.

### Goal: 

Analyze seasonality in electricity consumption by **hour** of day and **weekday**, so that investments can be targeted at true peak periods.

### Tasks:

- **Data ingestion & QA**: load raw consumption data, validate schema, and check for missing or anomalous values.  
- **Aggregation**: compute hourly and daily averages. 
- **Visualization**: export query results for plotting stacked time series and weekday x hour heatmaps.  
- **Interpretation**: identify the highest-stress periods for capacity planning.
  
---

## 📂 Data

*All data was sourced from Maven Analytics*

**`powerconsumption.csv`**  

Columns:  
    - `Datetime` (YYY-MM-DD HH:MM:SS)  
    - `PowerConsumption_Zone1`  
    - `PowerConsumption_Zone2`  
    - `PowerConsumption_Zone3`  

Source: hourly metered demand from January 2016 through December 2016.

---

## 🚀 How to Open & Use

1. **Clone the repo**
 
 ```bash
git clone https://github.com/la-retrouvaille/data-analysis-projects.git
   cd electricity-usage-analysis
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
jupyter notebook
``` 

Open `Electricity_Usage_Analysis_notebook.ipynb` and run all cells.

---

## 🔍 Key Findings

- **Hourly Electricity Consumption by Zone - Jan 2017**

   - **Zone contributions:** Zone 1 consistently accounts for roughly 40-45 MWh of the peak total load, Zone 2 for ~20-25 MWh and Zone 3 for ~20-30 MWh, making Zone 1 the dominant driver of system stress.
   
   - **Mid-month anomaly (~16-18 Jan):** A noticeable extra bump-total load just exceeds 100 MWh one evening-suggests an unusual event or extreme weather spike; worth investigating further.
   
   - **Weekend vs. weekday (visually):** Although overlaid, you can see weekend lines sit slightly below weekday peaks, implying a modest (~5-10%) drop in aggregate consumption on Saturdays and Sundays.

   ![Hourly Electricity Consumption by Zone - Jan 2017](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/Hourly%20Electricity%20Consumption%20by%20Zone%20-%20Jan%202017.PNG)

- **1 Jan 2017 Hourly Trend**

  - **Pre-dawn trough (04:00-07:00):** All three zones dip to their lowest levels: Zone 1 around 20 MWh, Zones 2 & 3 around 13-14 MWh; reflecting minimal overnight demand.
   
  - **Morning recovery (08:00-12:00):** Sharp jump in usage-Zone 1 surges to ~40 MWh, Zones 2 & 3 to ~25–26 MWh-when lighting, cooking and HVAC all coincide.
   
  - **Evening peak (18:00-20:00):** Although overlaid, you can see weekend lines sit slightly below weekday peaks, implying a modest (~5-10%) drop in aggregate consumption on Saturdays and Sundays.
 
  - **Post-peak decline (21:00-23:00):** Gradual wind-down as activity tapers off, but still double the overnight minimum.
  
  ![1 Jan 2017 Hourly Trend](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/Hourly%20Electricity%20Consumption%20by%20Zone%20-%2001%20Jan%202017.PNG)
    
- **Weekday x Hour Heatmap**

  - **Peak "hour of day":** 19:00-20:00 is the hottest block across every weekday, with average consumption here ~20-25% above the 24-hour mean.
  - **Pre-morning low:** 05:00-06:00 is the coolest slot, again uniformly across days.
  - **Weekday consistency:** Monday through Friday follow nearly identical profiles. Monday is only marginally higher, suggesting no single "worst" weekday.
  - **Weekend dip:** Saturday and Sunday sit about 10–15% below weekday evenings; Sunday mornings are particularly low, reflecting reduced commercial activity.

  ![Weekday x Hour Heatmap](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/Power%20Consumption%20by%20Day%20of%20Week%20and%20Hour.PNG)

---

## **Implications for Capacity Planning**

1. **Invest in evening capacity:** Systems must be sized (or flexibly contracted) to handle the 19:00-20:00 surge, especially in Zone 1.
2. **Target Zone 1 first:** Its outsized share of peak load makes it the highest-priority candidate for upgrades or demand-response programs.
3. **Monitor mid-month anomalies:** Investigate weather or operational incidents around January 16-18 to anticipate future spikes.
4. **Leverage weekend buffer:** Lower weekend load could be opportunities for maintenance windows or shifting non-critical operations offline.

---

## 📁 Folder Structure (Git Repo)

- **Electricity-Usage-Analysis/**

  - [Electricity_Usage_Analysis_notebook.ipynb](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/Electricity_Usage_Analysis_notebook.ipynb) <- Jupyter Notebook with Code & Visualizations

  - [powerconsumption.csv](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/powerconsumption.csv) <- Source Data

  - [Hourly Electricity Consumption by Zone - 01 Jan 2017.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/Hourly%20Electricity%20Consumption%20by%20Zone%20-%2001%20Jan%202017.PNG) <- Screenshot
 
  - [Hourly Electricity Consumption by Zone - Jan 2017.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/Hourly%20Electricity%20Consumption%20by%20Zone%20-%20Jan%202017.PNG) <- Screenshot
 
  - [Power Consumption by Day of Week and Hour.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/Power%20Consumption%20by%20Day%20of%20Week%20and%20Hour.PNG) <- Screenshot
 
  - [requirements.txt](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/requirements.txt) <- Requirements to run 

  - [.gitignore](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/.gitignore) <- Git rules: files/directories to ignore

  - [README.md](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Electricity-Usage-Analysis/README.md) <- This file  

---

## 💻 Tech Stack & Dependencies

- Python 3.x
- pandas (data manipulation)
- matplotlib & seaborn (visualization)
- Jupyter Notebook (interactive analysis)

---

## 💡 Next Steps & Optional Enhancements
 
- **External data:** enrich with weather (temperature, humidity) to explain variability.
  
- **Dashboard:** build an interactive Power BI or Dash app for real-time monitoring.

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
