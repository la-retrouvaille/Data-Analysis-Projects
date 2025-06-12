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

> *Note: As the raw listings data was too big to upload on github, I've only uploaded the Paris sample. However the whole overview along with any step can be found on `AirBnB_Listings_Analysis_notebook.ipynb`*

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
jupyter notebook
``` 
Open `AirBnB_Listings_Analysis_notebook.ipynb` and run all cells.

---

## 🔍 Key Findings

- **Élysée as most expensive neighbourhood**  

The Élysée district tops the list at €210.54, followed by Louvre (€175.38) and Passy (€161.14). This concentration in the city center reflects premium demand and limited supply in historic arrondissements.

![Average Listing Price by Paris Neighbourhood](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/Average%20Listing%20Price%20by%20Neighbourhood.PNG)

- **Relationship between capacity and price**
  
There's a strong positive relationship between capacity and price. Studios (1 guest) average €79.52, two-guest flats hit €155.10, four‑guest apartments €212.10, and larger units (6-8 guests) climb to €356-€406.

![Average Listing Price by Accommodates](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/Average%20Listing%20Price%20by%20Accommodates.PNG)
    
- **New Hosts & Average Price Over Time**

  - Host registrations rose steadily from 4 in 2008 to a peak of 12,147 in 2015. After the 2015 regulatory changes, new listings dropped ~27%, falling to 8,871 in 2016.

    ![New Airbnb Hosts over time](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/New%20Airbnb%20Hosts%20over%20time.PNG)
  
  - Prices were around €100 in 2014, ticked up to €103 in 2015, and then climbed further into the €130-€140 range by 2018-2020, indicating that while supply growth slowed, pricing power remained strong.

     ![Average Price over time](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/Average%20Price%20over%20time.PNG)

    
- **2015 Regulations Lead to Fewer New Hosts, Higher Prices**

 Host growth sharply declines post-regulation, yet average prices continue an upward trajectory; highlighting that regulatory caps constrained supply without depressing price levels.
 
  ![2015 Regulations](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/2015%20Regulations.PNG)

---

## 📁 Folder Structure (Git Repo)

- **AirBnB-Listing-Analysis/**

   - [Screenshots/](https://github.com/la-retrouvaille/Data-Analysis-Projects/tree/main/AirBnB-Listing-Analysis/Screenshots) <- Output Charts

     -[Average Listing Price by Neighbourhood.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/Average%20Listing%20Price%20by%20Neighbourhood.PNG)

     -[Average Listing Price by Accommodates.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/Average%20Listing%20Price%20by%20Accommodates.PNG)

     -[New Airbnb Hosts over time.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/New%20Airbnb%20Hosts%20over%20time.PNG)

     -[Average Price over time.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/Average%20Price%20over%20time.PNG)

     -[2015 Regulations.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/Screenshots/2015%20Regulations.PNG)

  - [paris_listings_sample.csv](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/paris_listings_sample.csv) <- Sample Data

  - [AirBnB_Listings_Analysis_notebook.ipynb](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/AirBnB_Listings_Analysis_notebook.ipynb) <- Jupyter Notebook with Code & Visualizations
 
  - [requirements.txt](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/requirements.txt) <- Requirements to run 

  - [.gitignore](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/.gitignore) <- Git rules: files/directories to ignore

  - [README.md](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/AirBnB-Listing-Analysis/README.md) <- This file  

---

## 💻 Tech Stack & Dependencies

- Python 3.x
- pandas (data manipulation)
- matplotlib & seaborn (visualization)
- Jupyter Notebook (interactive analysis)

---

## 💡 Next Steps & Optional Enhancements
 
- **Expand to other neighbourhoods/cities**: replicate the same pipeline for other neighbourhoods in Paris or with data from other cities
  
- **Version large data**: integrate Git LFS or DVC for the full Listings.csv
  
- **Build an interactive dashboard**: use Power BI to share insights with leadership
  
- **Deepen analysis**: incorporate host ratings, review counts, and seasonality factors

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
